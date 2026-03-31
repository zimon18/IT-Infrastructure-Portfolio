<img width="947" height="720" alt="image" src="https://github.com/user-attachments/assets/1cdeec41-d4fb-40e2-b861-0ec7853ef07b" /><img width="768" height="572" alt="image" src="https://github.com/user-attachments/assets/cb70f464-5ad3-4537-a929-e26aa0468868" /># Serwer plików SMB w W2012R2 #

## Tutoriale ##

### Instalacja i Konfiguracja AD i DNS ###

Przechodzimy do menedżera serwera i klikamy dodaj role i funkcje 

<img width="921" height="619" alt="image" src="https://github.com/user-attachments/assets/65f12ba9-faac-42c6-91bb-842aff8fbb0f" />


Pojawi się strona informująca nas do czego służy ten kreator 

<img width="932" height="632" alt="image" src="https://github.com/user-attachments/assets/5c9f22b6-689c-4107-9c6f-8cab3b221126" />


przechodzimy dalej 
Wybieramy czy instalacja ma być oparta na rolach czy usługach pulpitu zdalnego 
Zaznaczamy tutaj instalację opartą na rolach. Instalacja usług pulpitu zdalnego polega na instalowaniu funkcji na innych urządzeniach.

<img width="945" height="664" alt="image" src="https://github.com/user-attachments/assets/66ee1345-f3d4-4652-ada2-45c1bb18b6e2" />

Wybieramy na jakim serwerze mają zostać zainstalowane role 

<img width="936" height="667" alt="image" src="https://github.com/user-attachments/assets/a5fbfadd-f887-4d32-8c01-9d1372849b50" />

pojawia się lista ról, które możemy zainstalwoać 

<img width="941" height="661" alt="image" src="https://github.com/user-attachments/assets/7cebe595-5ce7-415e-8c4c-68d4ac4685f9" />

  
 
Wybieramy usługi domenowe Active Directory 

<img width="997" height="669" alt="image" src="https://github.com/user-attachments/assets/9bfa098a-0d33-49f3-a05e-e5198b0c2f4c" />


Klikamy Dodaj funkcje 

<img width="685" height="738" alt="image" src="https://github.com/user-attachments/assets/585c8ee3-48fb-4c81-b820-ad584fefe26e" />


a następnie dalej 
nie instalujemy żadnych dodatkowych funkcji dlatego klikamy Dalej

<img width="935" height="645" alt="image" src="https://github.com/user-attachments/assets/40ed27dd-c507-4dfe-95d1-7c85cf6a7b92" />

Dalej 

<img width="938" height="659" alt="image" src="https://github.com/user-attachments/assets/a153558b-763a-49d0-b989-dff7bf9890d7" />

pojawia się potwierdzenie i klikamy zainstaluj 

<img width="958" height="644" alt="image" src="https://github.com/user-attachments/assets/29d7f9ce-9d9a-457a-b3a3-c7207082a8c1" />

 
instalacja przebiegła pomyślnie  

<img width="958" height="676" alt="image" src="https://github.com/user-attachments/assets/a87113a8-86ab-44b8-bd19-45d5342cd986" />
 
 
teraz wymagana jest konfiguracja  
Na pulpicie nawigacyjnym pojawił się kafelek nowej usługi

<img width="945" height="590" alt="image" src="https://github.com/user-attachments/assets/d920521d-fe6b-40ff-af4e-d6c80cb2af01" />


pojawiło się też nowe narzędzie 

<img width="685" height="55" alt="image" src="https://github.com/user-attachments/assets/d2363bb0-5168-49bd-9587-7a4b1c228aeb" />


mamy też dostępną nową sekcję w ustawieniach 

<img width="957" height="688" alt="image" src="https://github.com/user-attachments/assets/3a060763-d733-4a76-aaab-3c96cb87d9e5" />


pojawiło się powiadomienie że wymagana jest konfiguracja usług domenowych 

<img width="590" height="428" alt="image" src="https://github.com/user-attachments/assets/c37c3645-63b5-428d-8505-c488ede012c0" />


Klikamy w napis Podnieś poziom tego serwera… 
Pojawiła się  konfiguracja wdrażania  

<img width="949" height="711" alt="image" src="https://github.com/user-attachments/assets/9569143f-3a45-48f6-934c-70e8ee0e0440" />


Na początku wybieramy czy chcemy dołączyć  do istniejącej domeny czy stworzyć nową.  
Nie mamy jednak do dyspozycji żadnej istniejącej domeny. Stworzymy więc nową. Dodamy 
ją do nowego lasu domen, czyli grupy. 
Domenę nazywam egzamin.zse 

<img width="927" height="670" alt="image" src="https://github.com/user-attachments/assets/78164ca7-7907-4394-997b-cc5d54c0b26f" />


klikam dalej  
teraz przechodzimy do opcji kontrolera domeny 

<img width="978" height="704" alt="image" src="https://github.com/user-attachments/assets/976ce30f-01cc-4156-aedf-ee7bfc2003c2" />


na samej górze wybieramy poziom funkcjonalności lasu, czyli jakie systemy mogą obsłużyć 
pełnię jej funkcji 
na razie zostawiamy windows server 2012 
Serwer DNS pozostawiamy zaznaczony  
teraz musimy podać hasło trybu przywracania usług katalogowych. 
użytkownik który ma takie uprawnienia może uzyskiwać dostęp do danych na temat 
funkcjonalności serwera.Koliber123 
Hasło powinno być inne niż hasło głównego administratora. 
Będzie to w tym przypadku Koliber321 

<img width="899" height="429" alt="image" src="https://github.com/user-attachments/assets/b5230a8a-76b2-45ab-8792-adb02e6c92dd" />


przechodzimy Dalej  
pojawi się komunikat o niemożności utworzenia delegowania dla serwera DNS 
Delegowanie to wysyłanie odpowiedzi na żądanie od komputerów klienckich 

<img width="989" height="228" alt="image" src="https://github.com/user-attachments/assets/cdcbaf60-82fd-4215-a83c-f95c052432bd" />


Klikamy dalej  
Teraz jest sprawdzane czy domena nie jest już wykorzystywana. 

<img width="1026" height="700" alt="image" src="https://github.com/user-attachments/assets/f3393fbb-22cd-44da-b68c-bf3bd6a8778f" />


nazwa domeny jest w porządku więc klikamy Dalej 

<img width="961" height="683" alt="image" src="https://github.com/user-attachments/assets/b5fe0946-0c66-4f73-9c4c-017ea6f26a93" />


W tym miejscu konfigurujemy foldery dla usług katalogowych, czyli dla danych o 
funkcjonowaniu serwera. 
Pozostawiamy je domyślnie jeżeli mamy jeden serwer 

<img width="953" height="681" alt="image" src="https://github.com/user-attachments/assets/dad2d1b7-1987-40af-90be-07782b539628" />


Przenosi nas do podsumowania 
klikamy dalej 

<img width="946" height="672" alt="image" src="https://github.com/user-attachments/assets/cb0c5b71-d627-4cf9-a9de-4d7ea75256c1" />


przenosi nas do weryfikacji konfiguracji 
w rozbudowanych sieciach może to potrwać bardzo długo, ale w małej sieci przebiegnie ona 
szybko 
klikamy zainstaluj 

<img width="933" height="689" alt="image" src="https://github.com/user-attachments/assets/5c755760-1f45-4c94-8a15-724ff7bd91fd" />

<img width="939" height="689" alt="image" src="https://github.com/user-attachments/assets/fb121aca-c9af-4c42-941e-435d8bebad2e" />



Po instalacji nastąpi ponowne uruchomienie  
podczas logowania zauważamy że przed nazwą Administrator pojawiła się nazwa domeny 

<img width="951" height="712" alt="image" src="https://github.com/user-attachments/assets/4ad07bc3-69fc-4ce9-85bf-6642dd806880" />


Po zalogowaniu widzimy, że pojawiły się teraz dwa nowe kafelki 

<img width="897" height="497" alt="image" src="https://github.com/user-attachments/assets/6cfce21d-a6b0-478e-9305-37001888cd4d" />


We właściwościach  serwera widzimy, że grupa robocza została zmieniona na domenę 

<img width="927" height="484" alt="image" src="https://github.com/user-attachments/assets/3c1a67df-efef-4d35-a493-1c0ccdd830b9" />

Aby zobaczyć czy serwer DNS został skonfigurowany poprawnie przechodzimy do sekcji 
DNS 
klikamy prawym przyciskiem  SERWER i uruchamiamy Menedżer DNS 

<img width="930" height="504" alt="image" src="https://github.com/user-attachments/assets/9e19bbfa-9da6-4259-8602-0b69ba038765" />


W menedżerze przechodzimy  serwer.egzamin.zse>Strefy wyszukiwania do 
przodu>egzamin.local 

<img width="946" height="304" alt="image" src="https://github.com/user-attachments/assets/31a9de28-ab92-4e52-b4e0-624bfaf99e97" />


Widzimy że obie karty sieciowe są podłączone 
można sprawdzić to też we Właściwościach serwer.egzamin.zse 

<img width="892" height="688" alt="image" src="https://github.com/user-attachments/assets/27c437b3-03a4-4b7a-9615-49e4a9e14570" />

<img width="642" height="782" alt="image" src="https://github.com/user-attachments/assets/cfccb2b2-3bc5-431f-91a5-952cbd4c06d6" />


### Instalacja i Konfiguracja DHCP ###

Teraz instalujemy trzecią rolę tym samym sposobem co poprzednie 
wybieramy serwer 

<img width="977" height="685" alt="image" src="https://github.com/user-attachments/assets/a4744b76-bf3d-4053-904f-1db53df9db09" />


wybieramy funkcję serwer DHCP 

klikamy Dodaj funkcję  
<img width="972" height="671" alt="image" src="https://github.com/user-attachments/assets/794fa987-9763-499d-a393-96a873aea58c" />

a następnie przechodzimy Dalej 
nie instalujemy dodatkowych funkcji

<img width="980" height="651" alt="image" src="https://github.com/user-attachments/assets/42b855b5-a3fb-4449-bdfb-7faaaeb0f0ec" />

Klikamy zainstaluj  

<img width="948" height="716" alt="image" src="https://github.com/user-attachments/assets/0acd58de-730b-4ceb-a3a3-d52e0d54d00f" />


instalacja powiodła się  

<img width="919" height="632" alt="image" src="https://github.com/user-attachments/assets/5a72e0a3-b097-4f0f-b4e7-f741477bcdec" />

przechodzimy do powiadomień 

<img width="768" height="572" alt="image" src="https://github.com/user-attachments/assets/b91179f9-cf33-4520-92e9-71cadc49fa8e" />

tym razem dokończymy jednak konfigurację innym sposobem 
w narzędziach wybieramy DHCP 

<img width="795" height="493" alt="image" src="https://github.com/user-attachments/assets/b7f14abb-2a0f-419e-8ee1-445138f15f4f" />


rozwijamy teraz serwer.so.local 

<img width="957" height="623" alt="image" src="https://github.com/user-attachments/assets/650169a3-e779-4fb4-be0b-185a687669df" />


na serwer egzamin.local klikamy prawym przyciskiem i włączamy autoryzację 

<img width="838" height="700" alt="image" src="https://github.com/user-attachments/assets/4971683e-f916-473c-b4b1-38be1922e4de" />


po rozwinięciu serwera pojawiły się protokoły IPv4 i IPv6 
IPv6 nie będzie potrzebne w naszej domenie, więc konfigurujemy jedynie IPv4
Pojawiają się informacje o tym jak skonfigurować serwer DHCP 

<img width="630" height="653" alt="image" src="https://github.com/user-attachments/assets/126642f8-50fd-430d-8426-d16f12d8d681" />

klikamy na IPv4 prawym przyciskiem  i wybieramy nowy zakres 

<img width="756" height="587" alt="image" src="https://github.com/user-attachments/assets/ac153c25-bad5-49ae-905c-9ab107f8df83" />


Uruchomi się kreator nowych zakresów 

<img width="878" height="673" alt="image" src="https://github.com/user-attachments/assets/507841c3-e63d-4546-8b14-91825f2fc2d6" />


W nazwie najlepiej podać nazwę domeny  

<img width="815" height="647" alt="image" src="https://github.com/user-attachments/assets/0d698385-653f-4ba8-bef0-8d8f5f81121b" />


posiłkując się topologią wiemy, że początkowy adres IP powinien wynosić 10.0.0.11, 
końcowy można ustawić jako np 10.0.0.199 
Długość to okres, po którym adresy ulegają zmianie  
Maskę podsieci ustawiamy na 255.255.255.0 ponieważ 255.0.0.0 mieści za dużo hostów 
Przechodzimy Dalej 
Teraz będziemy  tworzyć wykluczenia, czyli adresy, których nie przydziela serwer, tylko są 
one przydzielane ręcznie.
W tej sieci są to dwie drukarki. 
Są to pojedyncze adresy dlatego wpisujemy je na początku i na końcu adresu 

<img width="895" height="691" alt="image" src="https://github.com/user-attachments/assets/dfef730c-d3e9-44da-b092-ba8de67300d2" />


Przechodzimy dalej. Można w tym miejscu zmienić czas dzierżawy, ale tego nie będziemy 
robić 

<img width="841" height="646" alt="image" src="https://github.com/user-attachments/assets/f10ab024-8f15-4dd3-b52c-a65d47404796" />


Potwierdzamy i przechodzimy Dalej 

<img width="872" height="691" alt="image" src="https://github.com/user-attachments/assets/08cbc083-53f3-48b9-ba60-77c8aa9e1cae" />


Podajemy bramę domeny czyli najniższy adres z puli 

<img width="908" height="698" alt="image" src="https://github.com/user-attachments/assets/6884412b-aca4-47a8-8f57-997459a6ccc4" />


Przechodzimy dalej 
ustawiamy nazwę serwera “serwer” 
Adres IP ustawiamy na 10.0.0.1 i klikamy dodaj 

<img width="885" height="695" alt="image" src="https://github.com/user-attachments/assets/c7c67da5-4036-4421-b24f-91a72ac3f282" />

<img width="721" height="276" alt="image" src="https://github.com/user-attachments/assets/0e5ea953-987e-4e55-9cbc-027fde38da1f" />


Teraz widzimy obie karty sieciowe 

<img width="830" height="667" alt="image" src="https://github.com/user-attachments/assets/25ee4c2c-6ed8-492c-a8f5-b167e6eef926" />


Klikamy dalej 
Możemy teraz skonfigurować serwer WINS.  
Tłumaczy on adresy w sieci lokalnej 
nie ma potrzeby konfigurowania go teraz więc klikamy dalej 

<img width="917" height="703" alt="image" src="https://github.com/user-attachments/assets/03d7b534-9a23-4341-ad29-e099f8fbb664" />


i przechodzimy Dalej 

<img width="993" height="725" alt="image" src="https://github.com/user-attachments/assets/9a62fe39-2b02-482c-93c8-5ac277ae75ec" />


Zakończ 

<img width="994" height="741" alt="image" src="https://github.com/user-attachments/assets/5dd7b9bd-1943-43fa-afe9-1775842f88ef" />


Pojawiła się nowa sekcja - Zakres 

<img width="1096" height="673" alt="image" src="https://github.com/user-attachments/assets/d1c4eaa0-0932-4f84-9bbe-baeb545e113a" />


Zamykamy wszystkie okna i uruchamiamy serwer ponownie 

<img width="978" height="632" alt="image" src="https://github.com/user-attachments/assets/0cfccbb8-41bd-47c3-9ec0-54aaae0f667f" />


Należy teraz chwilę poczekać 

<img width="933" height="691" alt="image" src="https://github.com/user-attachments/assets/14cc2b10-a71e-441d-bdb6-3b14229f7db4" />


W powiadomieniach nadal mamy informacje o dalszej konfiguracji DHCP 
klikamy Dokończ 

<img width="597" height="311" alt="image" src="https://github.com/user-attachments/assets/adfb247e-27f1-4c8c-8941-79341fd64621" />


Określamy w jaki sposób będzie autoryzowany dostęp do serwera 

<img width="948" height="218" alt="image" src="https://github.com/user-attachments/assets/fedf0840-9ea6-427c-812d-333798545fae" />


możemy to pominąć 

<img width="779" height="314" alt="image" src="https://github.com/user-attachments/assets/9453c8d2-084a-4cf2-aa08-7bdc46454efe" />


zamykamy  

<img width="961" height="659" alt="image" src="https://github.com/user-attachments/assets/3d52c49b-208e-4f75-bce6-f286ba789e89" />


Jeżeli DHCP zostało skonfigurowane poprawnie powinny pojawić się zielone strzałki przy 
adresach IPv4 i IPv6 

<img width="1011" height="438" alt="image" src="https://github.com/user-attachments/assets/8ee71106-a522-4799-a881-735aee216a55" />


### Instalacja SMB ###

Przechodzimy do Menedżera serwera 
Klikamy Dodaj role i funkcje 

<img width="977" height="779" alt="image" src="https://github.com/user-attachments/assets/e929f3c1-d58b-4e28-9849-2f4c4acaf54b" />


Instalacja oparta na rolach 

<img width="976" height="699" alt="image" src="https://github.com/user-attachments/assets/78f1382d-9886-47d5-9015-0ea23190e0c5" />


Wybieramy też oczywiście serwer 

<img width="1008" height="703" alt="image" src="https://github.com/user-attachments/assets/96493f16-9f59-4184-8839-cf0a246b7828" />


Szukamy roli Usługi plików i magazynowania 
na razie zainstalowana jest 1 z 11 funkcji 

<img width="621" height="560" alt="image" src="https://github.com/user-attachments/assets/3b342e1b-e62c-4865-a8ea-94289267f54f" />


zaznaczamy te 3 funkcje 
 
<img width="530" height="170" alt="image" src="https://github.com/user-attachments/assets/8c129b3f-ca51-4c38-901b-b1a3c8018ba7" />

 
przechodzimy dalej 

<img width="990" height="624" alt="image" src="https://github.com/user-attachments/assets/c4d081a3-0121-46ea-916f-d31864a62aed" />

 
niczego innego już nie dodajemy 

<img width="1013" height="745" alt="image" src="https://github.com/user-attachments/assets/4d20e8a7-fd5c-433c-89b7-25c4182583b2" />


klikamy zainstaluj 

<img width="963" height="670" alt="image" src="https://github.com/user-attachments/assets/01c12fad-b5f0-4fce-aa19-2cb34c7989b5" />



trwa instalacja, po jej zakończeniu klikamy Zamknij 

<img width="959" height="671" alt="image" src="https://github.com/user-attachments/assets/accd58b2-5295-4b51-8cfc-6807408f875a" />


przechodzimy do menedżera serwera i wybieramy Usługi plików i magazynowania 

<img width="968" height="715" alt="image" src="https://github.com/user-attachments/assets/aeee232c-a9c8-4f1c-af12-e9d4f75d88ec" />

<img width="967" height="684" alt="image" src="https://github.com/user-attachments/assets/6eb8d757-fd02-46df-b762-463a23a9fe19" />


Przechodzimy do sekcji udziały 

<img width="971" height="580" alt="image" src="https://github.com/user-attachments/assets/fa5b100b-cba9-4c3a-9e4c-2ca485f3497c" />


rozwijamy Zadania i wybieramy nowy udział 
 

<img width="985" height="665" alt="image" src="https://github.com/user-attachments/assets/41c22b29-48f5-4044-8612-f0b2353b6b83" />

 
wybieramy szybkie SMB 

<img width="1017" height="713" alt="image" src="https://github.com/user-attachments/assets/a32430fa-782c-4a7e-9963-9f662c1c89aa" />

 
tworzymy ścieżkę na dysku D i nazywamy ją zasoby 

<img width="1009" height="677" alt="image" src="https://github.com/user-attachments/assets/cc154bf0-c641-4eb8-918e-630caf22fe50" />

<img width="992" height="722" alt="image" src="https://github.com/user-attachments/assets/7df7dd0f-e458-4e46-9fae-2bf50c43f8a4" />


klikamy OK 

<img width="1024" height="760" alt="image" src="https://github.com/user-attachments/assets/2969bb6a-c0cb-4f38-8d73-138ad7a1e0c8" />



zezwalamy na drugą opcję i przechodzimy dalej  

<img width="1043" height="698" alt="image" src="https://github.com/user-attachments/assets/d2489daf-dd6e-417d-a176-f7e20f924ccd" />


teraz przydzielimy uprawnienia jednemu z użytkowników 

<img width="1025" height="698" alt="image" src="https://github.com/user-attachments/assets/1dd2725f-912f-436b-afd4-dfaad47dc6e1" />


klikamy dostosowywanie uprawnień 
a następnie dodaj 

<img width="995" height="655" alt="image" src="https://github.com/user-attachments/assets/b42dae6d-26d2-4a07-a98e-22633183a9bc" />


Następnie hiperłącze Wybierz podmiot zabezpieczeń 

<img width="1013" height="664" alt="image" src="https://github.com/user-attachments/assets/9d23552c-1bb5-4789-bb45-80121b3031c5" />


pojawia się takie okno 
możemy od razu wpisać nazwę użytkownika bądź też wybrać go zaawansowanym sposobem

<img width="956" height="505" alt="image" src="https://github.com/user-attachments/assets/e2e422aa-c8fe-4905-bc3a-ec72da1314c0" />


Klikamy Znajdź teraz 

 <img width="1002" height="1029" alt="image" src="https://github.com/user-attachments/assets/fd6332ca-ca2d-4843-a99c-5a11a0519e9f" />

 
pojawiła się lista użytkowników 

<img width="894" height="366" alt="image" src="https://github.com/user-attachments/assets/d95be44a-ec68-4a45-927f-613cfb233166" />
 
 
Wybieramy na przykład użytkownika Piotr Jajo 
D<img width="946" height="964" alt="image" src="https://github.com/user-attachments/assets/8cea01cd-974d-4e22-95c9-1539a4788013" />


klikamy OK 

<img width="982" height="1034" alt="image" src="https://github.com/user-attachments/assets/4a2263b4-d65f-4df7-acbc-4610b6c8b288" />


w polu do wpisania pojawiła się nazwa obiektu  

<img width="961" height="503" alt="image" src="https://github.com/user-attachments/assets/263b6bda-d963-4c91-b5a7-afaa3b7e79b8" />


nadajemy tylko prawo odczytu i klikamy OK 

<img width="951" height="652" alt="image" src="https://github.com/user-attachments/assets/1e43fafb-9caa-4cf1-8ed1-29185403f84b" />


teraz usuwamy wpisy odnośnie innych grup/używkowników 
zaznaczamy interesujący nas wpis i klikamy Wyłącz dziedziczenie 
chcemy usuąć wszystkie uprawnienia 

<img width="991" height="688" alt="image" src="https://github.com/user-attachments/assets/de310261-dd35-4ac3-85a4-f548bfc9ca64" />


dodajemy jeszcze administratora z pełną kontrolą 

<img width="1050" height="590" alt="image" src="https://github.com/user-attachments/assets/4bed0805-94d0-4708-8c5c-5f1758201da5" />

<img width="1001" height="634" alt="image" src="https://github.com/user-attachments/assets/dd3cef18-c3b0-42c4-a308-9d0b47c80b92" />

<img width="962" height="644" alt="image" src="https://github.com/user-attachments/assets/ab69cd9f-a218-4354-98d7-1c23d838b9b6" />

<img width="992" height="666" alt="image" src="https://github.com/user-attachments/assets/7ec52643-0f63-4fc9-8c4c-15f2b2e3ec2a" />

klikamy zastosuj i OK 
przechodzimy dalej 

<img width="982" height="698" alt="image" src="https://github.com/user-attachments/assets/93c0edc5-c243-4bd8-aa2e-063ce5373e35" />

pojawia się takie podsumowanie  
jeżeli wszystko się zgadza klikamy Utwórz 

<img width="995" height="679" alt="image" src="https://github.com/user-attachments/assets/e5f09b57-944e-4c34-96e7-0780462df894" />
 
gdy się uda klikamy Zamknij  

<img width="998" height="636" alt="image" src="https://github.com/user-attachments/assets/b7841522-5870-4e7e-ac37-f3469fbb6d82" />

w menedżerze serwera pojawił się dodany folder 

<img width="991" height="585" alt="image" src="https://github.com/user-attachments/assets/3c32b234-90e1-4a64-b792-e0d4b9644c5c" />

klikamy prawym przyciskiem myszy i wybieramy Konfiguruj przydział 

<img width="1004" height="643" alt="image" src="https://github.com/user-attachments/assets/bca2e1e2-97db-48d2-ad4b-af9e55b3b2c8" />

wybieramy 1000 MB i klikamy OK 
widizmy że przydzielone jest teraz 100 MB 

<img width="923" height="687" alt="image" src="https://github.com/user-attachments/assets/d0526e55-27b2-4b4b-9c24-1232a0f7aed6" />

Sprawdźmy teraz działanie serwera na maszynie klienckiej  
Logujemy się na konto Piotr Jajo 

<img width="923" height="687" alt="image" src="https://github.com/user-attachments/assets/6c072ca2-cb51-4e91-8087-596cf9e5d33b" />

przechodzimy do eksploratora plików
i wpisujemy tam \\serwer\zasoby 

<img width="954" height="724" alt="image" src="https://github.com/user-attachments/assets/ae9f0b00-a168-4e8f-9b1f-25c88b4c67a9" />


gdy administrator doda aplikację do tego folderu użytkownik piotr jajo nie będzie mógł go 

<img width="947" height="720" alt="image" src="https://github.com/user-attachments/assets/a51bc1ac-89d2-4cf7-bae2-5f18ba814355" />

uruchomić ponieważ ma tylko prawo do odczytu 
natomiast gdy dodamy tam plik tekstowy możemy go otworzyć bez problemu 

<img width="1008" height="747" alt="image" src="https://github.com/user-attachments/assets/db4875b2-bc9b-45e4-834d-486577761178" />


aby ułatwić otwieranie tego folderu możemy skorzystać z opcji mapuj dysk sieciowy  

<img width="965" height="711" alt="image" src="https://github.com/user-attachments/assets/111b47b7-ecd2-4a34-bec8-06bf72ccf3cb" />

Wybieramy literę dysku (np. Z) wpisujemy \\serwer\udział  i klikamy Zakończ 

<img width="910" height="686" alt="image" src="https://github.com/user-attachments/assets/41a5eb54-529c-4c79-aaf7-16ffef3bf835" />

Folder pojawił się jako dysk Z 

<img width="935" height="680" alt="image" src="https://github.com/user-attachments/assets/03cf757d-d85d-474a-ba45-608c6cb0e418" />

<img width="1034" height="477" alt="image" src="https://github.com/user-attachments/assets/9c10e536-4351-41f5-b8ce-c3358e44497b" />

folderem możemy zarządzać też z innego miejsca 
Na serwerze uruchamiamy Narzędzia administracyjne a następnie Zarządzanie komputerem 

<img width="995" height="653" alt="image" src="https://github.com/user-attachments/assets/6fd89ecc-9b0e-4925-bbae-321f0ef26993" />

widzimy w odpowiedniej zakładce nasz folder 
widzimy że występują też ukryte foldery oznaczone znakiem dolara 

<img width="932" height="675" alt="image" src="https://github.com/user-attachments/assets/c4abfe86-2411-425d-8518-f466251572d8" />


spróbujemy teraz utworzyć taki folder 
klikamy PPM i wybieramy Nowy udział 

<img width="976" height="935" alt="image" src="https://github.com/user-attachments/assets/25f18ec4-1874-4165-b702-d6c5643d4ac8" />

przechodzimy dalej 

<img width="928" height="720" alt="image" src="https://github.com/user-attachments/assets/167ecdb1-c814-4733-bdad-00b312f8d946" />

wpisujemy d:\ukryty$ i przechodzimy Dalej 
oczywiście jeżeli nie mamy takiej ścieżki to tworzymy ją w tej chwili 

<img width="1054" height="821" alt="image" src="https://github.com/user-attachments/assets/75f3a393-62d8-4f5e-9482-18fb01cc51be" />

klikamy Dalej 

<img width="853" height="679" alt="image" src="https://github.com/user-attachments/assets/eefa4185-55d9-4fc0-8f24-918d6f3fc7b8" />


i Zakończ 

<img width="963" height="659" alt="image" src="https://github.com/user-attachments/assets/d81b770c-e219-40d5-8bfd-6024fbd7a99d" />

pojawi się jeszcze podsumowanie  
klikamy jeszcze raz zakończ 

<img width="932" height="686" alt="image" src="https://github.com/user-attachments/assets/3d0128ba-aede-4172-8df3-289340eafe0c" />

pojawił się nowo dodany folder  

<img width="1029" height="702" alt="image" src="https://github.com/user-attachments/assets/e9c95353-ecfb-41a5-816e-e89945477459" />

folder nie pokazuje się gdy przejdziemy do zasobów sieciowych 

<img width="994" height="706" alt="image" src="https://github.com/user-attachments/assets/50306582-5657-4749-a1c6-237f4f3b161d" />


możemy jednak go otworzyć wpisując bezpośrednio jego lokalizację czyli \\serwer\ukryty$

<img width="1003" height="714" alt="image" src="https://github.com/user-attachments/assets/cd1d42ad-15cf-45b2-aa9f-e89b2804551c" />


Zadania 
1. Utwórz na serwerze dwóch użytkowników oraz folder o 
nazwie "SSO1". 
Na początku utworzymy dwa konta użytkowników 
Przechodzimy do Menedżera Serwera 
z Menu Narzędzia wybieramy Użytkownicy i komputery Active Directory 
Przechodzimy do jednostki Users 
klikamy ppm nowy>Użytkownik 
pojawia się okno tworzenia użytkownika 
nazywamy go  
Bastian Smok 
z niewygasającym hasłem Orangutan123 
 
Klikamy Zakończ 
 
 
 
 
Następnie tym sposobem dodajemy użytkownika Dariusz Kubica z takim samym hasłem 
 
 
 
klikamy zakończ 
przechodzimy teraz na dysk D 
tworzymy nowy folder SSO1 
2. Udostępnij go z limitem 5 użytkowników i nadaj opis "Zajęcia 
lekcyjne z SSO". 
przechodzimy teraz do udziałów 
dodajemy nowy udział 
szybkie i dalej 
wpisujemy niestandardową ścieżkę D:\SSO1 
wszystko się zgadza, dodajemy też opis
dodajemy takie uprawnienia 
klikamy Dostosowanie uprawnień 
 
 
Wyłącz dziedziczenie 
 
 
 
usuwamy wszystko 
następnie klikamy Dodaj 
oraz Wybierz podmiot zabezpieczeń 
dodajemy utworzonych wcześniej użytkowników wpisując ich nazwy czyli bastian.smok oraz 
dariusz.kubica 
dostaje on prawo do odczytu (zad 4) 
bastian.smok natomiast nie będzie miał dostępu 
stosujemy zmiany 
przechodzimy dalej 
wszystko się zgadza więc klikamy utwórz 
Otwórz okno Konfigurowanie przydziału w celu ustawienia przydziau 
Wybieramy 100 MB i klikamy OK 
pojawił się przydział 
teraz klikamy prawym przyciskiem myszy na folder 
wybieramy właściwości 
Zakładka Udostępnianie 
Udostępnianie zaawansowane 
wpisujemy 5 i klikamy zastosuj 
3. Opublikuj folder "SSO1" w AD. 
folder pojawia się w zarządzaniu komputerem 
4. Jeden z tych użytkowników ma mieć prawo do odczytu do 
tego folderu, a drugi nie powinien mieć do niego dostępu. 
Sprawdzamy czy ustawienia wybrane podczas wykonywania zadania 2 zostały zastosowane 
na kliencie logujemy się jako Bastian Smok 
po wpisaniu lokalizacji \\serwer\sso1 pojawia się taki komunikat 
teraz logujemy się jako Dariusz Kubica 
w przypadku Dariusza udaje się otworzyć folder 
5. Utwórz na serwerze jeszcze czterech użytkowników oraz 
folder o nazwie "SSO2". 
Tak samo jak wcześniej tworzymy użytkowników i folder 
 
 
 

6. Wykonaj czynności z punktu 2-3 stosując je do folderu 
"SSO1". 
Tworzymy udział dla nowego folderu 
Dalej 

 
 
 
Wyłączamy dziedziczenie  
Klikamy następnie Dodaj  
wybierz podmiot zabezpieczeń 
wpisujemy Informatycy 
dodajemy pełnę kontrolę 
Widzimy że Informatycy mają pełną kontrolę 
kończymy kreację 
przydzielamy tak samo 100MB 


ustawiamy też limit dla 5 użytkowników 
7. Utwórz dwie grupy: "Informatycy" i "Elektronicy". 
Tworzymy grupę Informatycy oraz Elektronicy w tym samym miejscu co użytkowników 
PPM i dodaj grupę 
 
 
 
 
 
 
 
 
 
8. Przypisz użytkowników do tych grup, tak aby trzech z nich 
miało pełną kontrolę do obydwu folderów, a trzech pozostałych 
pełną kontrolę do folderu "SSO", a do "SSO2" brak dostępu. 
Informatycy będą mieli pełną kontrolę do obu folderów a elektronicy pełną kontrolę do sso1 i 
brak dostępu do sso2  
teraz dodajemy użytkowników do grup 
do grupy informatycy przejdą dariusz.kubica, adam.kwita i gniewomir.wielki 
do grupy elektornicy zostaną przydzieleni bastian.smok, andrzej.karcz i patryk.madej 
klikamy prawym przyciskiem myszy na każdego użytkownika i wpisujemy nazwę grupy do 
której chcemy go dodać 

będzie pojawiac się takie okienko potwierdzające 
takie są skutki 

teraz przydzielimy uprawnienia do sso1 
klikamy ppm i właściwości 
przechodzimy do zakładki uprawnienia i klikamy Dostosowywanie uprawnień 
pojawia się znany nam panel 
klikamy teraz usuń przy dariuszu kubicy 
i dodajemy pełną kontrolę dla obu grup 
klikamy zastosuj 
 
 
 
 
teraz sprawdźmy na klientach czy zmiany  
 
logujemy się na gniewomira 
 
 
 
 
należy on do grupy informatycy więc powinien mieć pełny dostęp do obu folderów 
w sso1 utworzył nowy dokument tekstowy 
widzimy że ma on pełną kontrolę nad oboma folderami 

teraz sprawdźmy możliwości patryka madeja, który należy do grupy elektronicy 
udało mu się otworzyć folder sso1 
do folderu sso2 jednak nie ma uprawnień więc wszystko się zgadza 
9. Utwórz jeden ukryty folder o dowolnej nazwie z prawami 
odczytu tylko dla użytkowników tych dwóch grup. 
W poradniku został pokazany sposób tworzenia ukrytych folderów i jak one działają  
tworzymy nowy udział 
lokalizacja to d:\tajny$ 
 
 
tworzymy ten folder 
 
 
 
Wybieramy Dostosowywanie uprawnień 
dodajemy Informatycy 
oraz dodajemy  
elektornicy tylko do odczytu 
klikamy OK a następnie zakończ 

z klienta możemy odczytać folder 
 
 
 
podczas próby utworzenia pliku tekstowego pojawiło się takie okno, które potwierdza że jest 
możliwy tylko odczyt 
 
 
 
oczywiście folder nie wyświetla się w tym miejscu 
