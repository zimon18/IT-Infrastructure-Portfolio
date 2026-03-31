# DNS BIND w Ubuntu Server 18.04 LTS

## Przygotowanie środowiska

Uruchamiamy maszynę z serewerem Ubuntu 18.04 

<img width="1067" height="802" alt="image" src="https://github.com/user-attachments/assets/fbde1467-5b96-439c-91c7-f67c5906bc49" />

Upewniamy się że mamy pierwszą kartę sieciową jako NAT a drugą jako sieć wewnętrzną 

<img width="836" height="149" alt="image" src="https://github.com/user-attachments/assets/5f170c99-5df9-471e-8a93-6c7fb6803127" />

na serwerze przechodzimy do pliku konfiguracyjnego interfejsów sieciowych w pliku 
`/etc/netplan/00-installer-config.yaml`

w tej chwili mamy jedynie pierwszą kartę sieciową oznaczoną jako `enp0s3` w tymże miejscu. 
możemy zostawić ją jako DHCP
<img width="1162" height="885" alt="image" src="https://github.com/user-attachments/assets/49aad860-0e15-4d25-88f7-347d9903824d" />

jednakże na drugiej karcie sieciowej musimy ustawić statyczny adres `10.0.66.10` 
ważne jest też by brama domyślna była inna niż serwer czyli w tym przypadku będzie to 
`10.0.66.1`

serwery dns ustawiamy na `8.8.8.8` i `8.8.4.4` 
<img width="1170" height="907" alt="image" src="https://github.com/user-attachments/assets/41474e5c-f33b-496f-8540-faaf5b813e27" />

po zapisaniu wpisujemy `netplan apply`  
<img width="1126" height="831" alt="image" src="https://github.com/user-attachments/assets/4b4fe926-8cd2-4760-b6d5-4e738fda4d02" />

nie pojawił się żaden błąd więc adresy zostały dobrze skonfigurowane 
na potwierdzenie  
<img width="1088" height="255" alt="image" src="https://github.com/user-attachments/assets/966aaabc-550f-47df-b8fa-4a00078b48dd" />

## Konfiguracja domeny i hostów

teraz możemy przejść do ustalenia nazwy domeny oraz nazwy hosta 
zrobimy to w pliku  `/etc/hosts` 
możemy otworzyć go za pomocą `mcedit`a
<img width="1075" height="800" alt="image" src="https://github.com/user-attachments/assets/1e49ece0-cd89-46ba-943a-e56842162644" />

nazwę serwera zmieniam na `serwer37v` natomiast nazwę domenu ustawiam na 
`s37.egzamin.local` 
skróconą nazwę serwera wpisujemy po jeszcze osobno po spacji  
<img width="1145" height="851" alt="image" src="https://github.com/user-attachments/assets/31556ce4-6b18-4df1-85dc-9ca6ed956b03" />

po zapisaniu pliku w takiej formie restartujemy serwer 

<img width="1032" height="733" alt="image" src="https://github.com/user-attachments/assets/aa294417-b313-4694-af43-69e1fd196da4" />

działa 

<img width="1159" height="864" alt="image" src="https://github.com/user-attachments/assets/6aff2c20-f7b3-4bbb-ac8e-44731234c9ec" />

ważne jest też dopisanie jednej rzeczy w pliku `/etc/default` 

## Instalacja serwera BIND9

teraz isntalujemy serwer dns za `apt-get install bind9 bind9utils`. 
potwierdzamy wybierając `y`
<img width="1171" height="567" alt="image" src="https://github.com/user-attachments/assets/7acb83fd-daed-4f25-9518-cf0cc82d6afa" />

warto jeszcze jest przejść do pliku `/etc/default/bind9` i dopisać linijkę, która zapobiegnie 
potencjalnym problemom ze statusem unreachable. 
 
 
dopisujemy parametre `-4` w ostatniej linijce 

<img width="1170" height="845" alt="image" src="https://github.com/user-attachments/assets/13e9c82f-4c47-45f3-bd35-7486f299ec2c" />

## Konfiguracja stref DNS

przechodzimy do katalogu `/etc/bind` 
<img width="1169" height="899" alt="image" src="https://github.com/user-attachments/assets/42cba140-6a62-40b1-9b79-e9895bdb2848" />

widzimy następujące pliki 

<img width="1150" height="845" alt="image" src="https://github.com/user-attachments/assets/f996e2ff-e6c0-4fcf-8d77-75f05f8b8a5d" />

przechodzimy do pliku `named.conf.options`  

<img width="1173" height="896" alt="image" src="https://github.com/user-attachments/assets/80e9f19f-f562-4b81-a312-7b9287e620f9" />

przechodzimy do pliku  

<img width="1169" height="938" alt="image" src="https://github.com/user-attachments/assets/df3b1dcd-a8a7-4f97-be61-8df402f42be7" />

musimy odkomentować linijkę `//forwarders` i adres zamienić na `8.8.8.8` 

sprowadzamy więc to do następującej postaci  

<img width="1162" height="919" alt="image" src="https://github.com/user-attachments/assets/d10aeb9d-314d-4064-b2ab-f3be84d9d9e8" />

zapisujemy  
<img width="1168" height="908" alt="image" src="https://github.com/user-attachments/assets/58bb9f69-ceae-4fd8-adce-eca9efcd022a" />

po wykonaniu tejże czynności restartujemy serwer oraz sprawdzamy jego status 

działa

<img width="1131" height="802" alt="image" src="https://github.com/user-attachments/assets/be715f45-bd1d-41ac-837e-4f0962e6bd78" />

wszystko w porządku jest gdy otrzymamy takie dane (status: NOERROR)  z polecenia  `dig -x 127.0.0.1`

<img width="1162" height="904" alt="image" src="https://github.com/user-attachments/assets/81bb47de-e993-44d6-9c36-74a40b5bf5ce" />

teraz musimy sprawdzić czy plik `/etc/bind/named.conf`  zawiera pewne wpisy 
przechodzimy do pliku

<img width="1133" height="830" alt="image" src="https://github.com/user-attachments/assets/b60f580a-9040-4995-86f7-c90616bf83ae" />

chodzi o 3 ostatnie linijki 

<img width="1134" height="847" alt="image" src="https://github.com/user-attachments/assets/2c040c7c-b674-4d9d-84f8-059d6b50b8a7" />

gdyby zdarzyło się, że ich nie ma musielibyśmy dodać je ręcznie 
wychodzimy z pliku bez zmian

<img width="1068" height="808" alt="image" src="https://github.com/user-attachments/assets/08e87cd8-a97e-44ba-bfae-d060315899a4" />

### Tworzenie stref wyszukiwania do przodu i tyłu

utworzymy teraz strefy wyszukiwania do przodu i do tyłu edytując plik  
`/etc/bind/named.conf.local`. 
w pliku na razie znajdują się takie dane 

<img width="1170" height="858" alt="image" src="https://github.com/user-attachments/assets/2e9a208d-64c1-4cdf-909d-51d8e55caf65" />

najpierw dodamy strefę wyszukiwania do przodu

<img width="1175" height="891" alt="image" src="https://github.com/user-attachments/assets/53f092c4-9a55-4417-8292-abaf256cdbb8" />

pod nią tworzymy strefę wyszukiwania do tyłu  
zapisujemy adres od tyłu z pominięciem ostatniego oktetu

<img width="1144" height="436" alt="image" src="https://github.com/user-attachments/assets/e1ae8657-d389-484c-936d-d73b3beb4187" />

plik zapisujemy w takiej formie  

<img width="1153" height="821" alt="image" src="https://github.com/user-attachments/assets/7578c2bc-52e2-42a4-b695-80d216042179" />

teraz musimy utworzyć pliki, które zapisaliśmy w konfiguracji 
wpisujemy `cp /etc/bind/db.local /etc/bind/for.egzamin.local`

<img width="1172" height="299" alt="image" src="https://github.com/user-attachments/assets/7fc4af47-fca1-4230-afc4-2143ddf99c7f" />

uruchamiamy plik za pomocą `mcedit`a

<img width="1102" height="431" alt="image" src="https://github.com/user-attachments/assets/fde560d7-c01d-49e6-8752-71e4397a6c12" />

pojawia się taki plik  

<img width="1159" height="839" alt="image" src="https://github.com/user-attachments/assets/bf7fdb81-a57d-43f7-ac13-a4af3ee1d2f6" />

dostosowujemy do do naszych potrzeb 
dodajemy nazwę domeny i aliasy naszych klientów wraz z adresami (pamiętając by ustawić 
takie same w następnych krokach) 
Ubuntu: `papryczka`, klient Windows: `pomidorek`

<img width="1160" height="853" alt="image" src="https://github.com/user-attachments/assets/77dbf53c-45b9-4550-808f-f9b4a9949205" />

zapisujemy i podobnie robimy z plikiem stref wyszukiwania do tyłu  

<img width="1154" height="459" alt="image" src="https://github.com/user-attachments/assets/a7fa68b7-6109-44dd-8bab-38e526c5739e" />

w pliku wprowadzamy takie zmiany 

<img width="1095" height="823" alt="image" src="https://github.com/user-attachments/assets/fac1dcd6-157e-4c4b-b732-0b59291e1330" />

restartujemy  
<img width="1138" height="175" alt="image" src="https://github.com/user-attachments/assets/e3c80088-9434-4453-8d75-bfabf9398ade" />

działa

<img width="1116" height="646" alt="image" src="https://github.com/user-attachments/assets/06327ae8-75f2-406d-be00-77a36b535bb2" />

inne polecenia nie wykazały również żadnych błędów 

## Rozwiązywanie problemów (Troubleshooting)

pozostają jeszcze 2 polecenia  

pierwsze z nich to  
<img width="889" height="76" alt="image" src="https://github.com/user-attachments/assets/cd49e85f-6feb-4b0f-a2b8-b3dafb4043da" />

pojawił się status `SERVFAIL` więc mamy problem 
<img width="1166" height="886" alt="image" src="https://github.com/user-attachments/assets/f9390da3-9c16-4f36-a9fa-8ac1ea8a3070" />

drugim poleceniem jest `nslookup serwer.egzamin.local` 
tutaj również mamy problem gdyż pokazuje nam stary adres 
<img width="1168" height="312" alt="image" src="https://github.com/user-attachments/assets/e8ca1a81-a3de-420a-9ab6-1ec12df23842" />

Aby naprawić błąd musimy zmienić wpisy w pliku `/etc/resolv.conf`  
Jednakże od wersji ubuntu 18.04 zmiany w tym pliku kasują się po restarcie systemu. Aby 
temu zaradzić usuniemy ten plik a następnie stworzymy go jeszcze raz, wpisując w nim 
odpowiednie dane. 

wpisujemy polecenie `rm /etc/resolv.conf` 

<img width="1149" height="243" alt="image" src="https://github.com/user-attachments/assets/04631d8b-a40c-405e-ad66-d52ec91fc7c0" />

następnie tworzymy ponownie ten plik w `mcedit`cie  

wprowadzamy następujące dane pasujące do naszej domeny 

<img width="1169" height="851" alt="image" src="https://github.com/user-attachments/assets/e080b179-abd3-494e-9007-9379b00ea952" />

powinniśmy jeszcze zablokować plik przed nadpisywaniem wpisując `sudo chattr +i /etc/resolv.conf`

<img width="1101" height="805" alt="image" src="https://github.com/user-attachments/assets/4b5442ec-7000-4c80-b4db-38148b0994c2" />

aby sprawdzić czy zadziałało rebootujemy  

<img width="1084" height="665" alt="image" src="https://github.com/user-attachments/assets/a329f530-03cc-4b71-a922-39403665f84e" />

widzimy że status zmienił się na `noerror` 

<img width="1124" height="794" alt="image" src="https://github.com/user-attachments/assets/b2d80d4d-fc1a-4406-b001-65b58ce5c407" />

tutaj również zmieniło się na lepsze  

<img width="1176" height="296" alt="image" src="https://github.com/user-attachments/assets/611f6fb2-8bb1-4a6c-8352-3e434454b0c6" />

sprawdzamy czy nasze hosty się zgadzają  

<img width="1179" height="606" alt="image" src="https://github.com/user-attachments/assets/36098744-1a66-4fe8-bef1-5f3420e241db" />

jest dobrze 

<img width="1174" height="681" alt="image" src="https://github.com/user-attachments/assets/3998309b-b708-4680-824a-d62fa59a29fa" />

## Konfiguracja maszyn klienckich

przechodzimy teraz do hostów 

pamiętajmy żeby w obu maszynach ustawić sieć wewnętrzną  

<img width="1152" height="874" alt="image" src="https://github.com/user-attachments/assets/2df69f56-1485-412f-acb4-8a05f38868f3" />

nadajemy karcie sieciowej dane pasujące do naszej podsieci 

<img width="1126" height="755" alt="image" src="https://github.com/user-attachments/assets/2a31caad-48c7-4dca-a4a9-93433a9c448c" />

pamiętajmy też by włączyć odnajdowanie sieci 

<img width="1166" height="859" alt="image" src="https://github.com/user-attachments/assets/b1b9a588-4b10-4ce0-974d-f67dcd780f50" />

ustawiamy adres na ubuntu  

<img width="1162" height="797" alt="image" src="https://github.com/user-attachments/assets/a20e2483-2d55-433e-9310-04c5188c4cdb" />

pingowanie po nazwach działa 

<img width="1156" height="759" alt="image" src="https://github.com/user-attachments/assets/52759725-83d5-44c0-bc83-1bf16551738d" />
<img width="1182" height="883" alt="image" src="https://github.com/user-attachments/assets/81f38ab8-92c6-4aa0-b759-c5e26a80ed8f" />

po adresach również 

<img width="1173" height="490" alt="image" src="https://github.com/user-attachments/assets/366cd716-04c7-4df3-a833-b37367a64b51" />
<img width="1164" height="820" alt="image" src="https://github.com/user-attachments/assets/9752cb8a-34cd-49b4-ad36-1b11138b60bc" />

teraz sprawdźmy czy pingowanie z klienta działa  
pojawił się błąd

<img width="1147" height="811" alt="image" src="https://github.com/user-attachments/assets/cc197ff9-4fce-414c-827e-0dfe36310c46" />

pingowanie samo w sobie działa ale serwer jest na adresie localhost 
 
<img width="1077" height="742" alt="image" src="https://github.com/user-attachments/assets/278db356-b2c2-436d-a5f5-118255f4f670" />

problem jest spowodowany przez plik `resolv.conf` 
uruchamiamy go  

<img width="1188" height="759" alt="image" src="https://github.com/user-attachments/assets/48f0cddc-8926-4caa-8d25-121b2f342735" />

podobnie jak na serwerze musimy usunąć ten plik i dodać go ponownie 

<img width="1168" height="733" alt="image" src="https://github.com/user-attachments/assets/19224024-5777-41c2-8d1e-9388d55c4972" />
<img width="1175" height="792" alt="image" src="https://github.com/user-attachments/assets/159452ec-6804-45a6-81c9-fdad2e32e786" />
<img width="1178" height="832" alt="image" src="https://github.com/user-attachments/assets/43547f5f-47da-49a8-8399-67aaabac28c2" />

pinguje do serwera i windowsa 

<img width="1044" height="771" alt="image" src="https://github.com/user-attachments/assets/e67fd5fc-84ef-4f9c-b18c-2484292ec754" />

`nslookup` działa
