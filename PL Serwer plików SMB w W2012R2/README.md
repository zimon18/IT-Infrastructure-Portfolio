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

<img width="936" height="626" alt="image" src="https://github.com/user-attachments/assets/9f5e62cc-cbca-4e71-a623-038d8aa3da22" />

Przechodzimy do jednostki Users 

<img width="942" height="678" alt="image" src="https://github.com/user-attachments/assets/ddd9af7e-2ae5-4427-b302-bf78e0b6651e" />

klikamy ppm nowy>Użytkownik 

<img width="938" height="595" alt="image" src="https://github.com/user-attachments/assets/b6ecaff1-2078-4058-ae70-0896f89e5f2d" />

pojawia się okno tworzenia użytkownika 

<img width="874" height="661" alt="image" src="https://github.com/user-attachments/assets/b8472cdd-145e-4f4a-aa6f-5badba74f946" />

nazywamy go  
Bastian Smok 
z niewygasającym hasłem Orangutan123 

<img width="916" height="675" alt="image" src="https://github.com/user-attachments/assets/a9bbce6d-6e2c-4e0a-8041-7198f08a6b92" />

Klikamy Zakończ 
 
 <img width="846" height="724" alt="image" src="https://github.com/user-attachments/assets/b2416528-26ce-4561-b492-32b670b793d6" />

 
 
 
Następnie tym sposobem dodajemy użytkownika Dariusz Kubica z takim samym hasłem 

<img width="775" height="623" alt="image" src="https://github.com/user-attachments/assets/811c914f-659d-44e6-b662-96b374b9fcb6" />
 
<img width="844" height="704" alt="image" src="https://github.com/user-attachments/assets/504dfbbb-5e70-4726-9de7-6e02b44a7c24" />
 
 
klikamy zakończ 

<img width="924" height="758" alt="image" src="https://github.com/user-attachments/assets/5d5fb216-c687-4832-a60c-c2448a0f5cbf" />

przechodzimy teraz na dysk D 

tworzymy nowy folder SSO1 

<img width="967" height="763" alt="image" src="https://github.com/user-attachments/assets/482e0400-be3b-47f2-9d7b-5577c233254c" />

2. Udostępnij go z limitem 5 użytkowników i nadaj opis "Zajęcia 
lekcyjne z SSO". 
przechodzimy teraz do udziałów

<img width="941" height="676" alt="image" src="https://github.com/user-attachments/assets/406257f5-942f-423f-b388-8547dbc82c1a" />

dodajemy nowy udział 

<img width="951" height="666" alt="image" src="https://github.com/user-attachments/assets/945401b9-b242-465c-a5e0-d5d14f6b0e70" />

szybkie i dalej 

<img width="934" height="686" alt="image" src="https://github.com/user-attachments/assets/90ed23ce-a3af-4b1e-9075-24efcae7b26e" />

wpisujemy niestandardową ścieżkę D:\SSO1 

<img width="967" height="635" alt="image" src="https://github.com/user-attachments/assets/d42ff1a5-ddfe-4883-aa27-0680b54549af" />

wszystko się zgadza, dodajemy też opis

<img width="966" height="650" alt="image" src="https://github.com/user-attachments/assets/0a5b0af7-8e10-4d5a-83b3-d66b9d636053" />

dodajemy takie uprawnienia 

<img width="992" height="676" alt="image" src="https://github.com/user-attachments/assets/45d59ffd-ec8f-4dfa-9a49-0f2ef3c8eb7b" />

klikamy Dostosowanie uprawnień 
 

<img width="1017" height="732" alt="image" src="https://github.com/user-attachments/assets/4047cb81-e88f-4c87-ad52-bc334787ecb9" />

Wyłącz dziedziczenie 

 <img width="939" height="634" alt="image" src="https://github.com/user-attachments/assets/53d9f7dc-4f6b-48ff-84b8-ed7f367d0d7b" />

 
 
usuwamy wszystko 

<img width="975" height="511" alt="image" src="https://github.com/user-attachments/assets/5388ed2b-8b8c-4f10-8c3b-089cdd78a001" />

następnie klikamy Dodaj 

<img width="965" height="626" alt="image" src="https://github.com/user-attachments/assets/8c0ae42e-c93a-40a2-8527-4d3b545905d0" />

oraz Wybierz podmiot zabezpieczeń 

<img width="1030" height="685" alt="image" src="https://github.com/user-attachments/assets/25775a3f-c3dd-431a-a7fc-39cea9c971bf" />

dodajemy utworzonych wcześniej użytkowników wpisując ich nazwy czyli bastian.smok oraz 
dariusz.kubica 

D<img width="959" height="510" alt="image" src="https://github.com/user-attachments/assets/12312340-2fc8-4213-9707-c8026d053e66" />

dostaje on prawo do odczytu (zad 4) 
bastian.smok natomiast nie będzie miał dostępu 

<img width="978" height="639" alt="image" src="https://github.com/user-attachments/assets/d02729f9-e05c-4d4e-aaa1-a9b9c0c9c122" />

stosujemy zmiany 

<img width="989" height="652" alt="image" src="https://github.com/user-attachments/assets/873388e0-ab97-4be5-8542-7792439c20f5" />

przechodzimy dalej 

<img width="974" height="669" alt="image" src="https://github.com/user-attachments/assets/aeca1bad-4f0f-4e3e-996c-ec1403e5b9d5" />

wszystko się zgadza więc klikamy utwórz 

<img width="978" height="686" alt="image" src="https://github.com/user-attachments/assets/c7eebf55-c531-4132-ade7-6e759e2061d0" />

Otwórz okno Konfigurowanie przydziału w celu ustawienia przydziau 

<img width="993" height="611" alt="image" src="https://github.com/user-attachments/assets/64519be8-3078-485e-b4ce-9d5bb9926b4f" />

Wybieramy 100 MB i klikamy OK 

<img width="988" height="988" alt="image" src="https://github.com/user-attachments/assets/ab4779c1-0bfc-4a60-bb30-485dc8182250" />

pojawił się przydział 

<img width="924" height="693" alt="image" src="https://github.com/user-attachments/assets/62c563b0-bc0e-44cb-a543-de726901bdbd" />

teraz klikamy prawym przyciskiem myszy na folder 
wybieramy właściwości 

<img width="1014" height="696" alt="image" src="https://github.com/user-attachments/assets/b919103c-3c34-4910-8a7e-e8dfeee8be40" />

Zakładka Udostępnianie 

<img width="940" height="916" alt="image" src="https://github.com/user-attachments/assets/40a44aee-c9b4-4b9e-a7c9-588e79aef851" />

Udostępnianie zaawansowane 

<img width="873" height="935" alt="image" src="https://github.com/user-attachments/assets/254dbe20-ff72-4f3c-83fa-4eb0bb4266c4" />

wpisujemy 5 i klikamy zastosuj 

<img width="686" height="703" alt="image" src="https://github.com/user-attachments/assets/4f0e8ad3-165d-4714-abfa-204432765d79" />

3. Opublikuj folder "SSO1" w AD. 
folder pojawia się w zarządzaniu komputerem

<img width="963" height="688" alt="image" src="https://github.com/user-attachments/assets/4d3f1313-46ab-43f6-b82c-1bf1c97b1976" />

4. Jeden z tych użytkowników ma mieć prawo do odczytu do 
tego folderu, a drugi nie powinien mieć do niego dostępu. 
Sprawdzamy czy ustawienia wybrane podczas wykonywania zadania 2 zostały zastosowane 
na kliencie logujemy się jako Bastian Smok

<img width="934" height="677" alt="image" src="https://github.com/user-attachments/assets/8bbe04ce-a97b-477f-a74c-6ca7013fca54" />

po wpisaniu lokalizacji \\serwer\sso1 pojawia się taki komunikat 

<img width="938" height="684" alt="image" src="https://github.com/user-attachments/assets/41751a37-0747-4801-a1ad-0c87e1554aaa" />

teraz logujemy się jako Dariusz Kubica 

<img width="929" height="692" alt="image" src="https://github.com/user-attachments/assets/9f84a8a0-9569-489e-ab68-4579a078c735" />

w przypadku Dariusza udaje się otworzyć folder 

<img width="938" height="736" alt="image" src="https://github.com/user-attachments/assets/ccd492d4-ab3c-4653-b0e0-d215f09033e5" />





5. Utwórz na serwerze jeszcze czterech użytkowników oraz 
folder o nazwie "SSO2". 
Tak samo jak wcześniej tworzymy użytkowników i folder

<img width="795" height="649" alt="image" src="https://github.com/user-attachments/assets/4e09f623-85d5-46d5-a895-a5ced3aa8ac4" />

<img width="868" height="668" alt="image" src="https://github.com/user-attachments/assets/c0e11ce8-6ebb-43f3-a875-92df061018fc" />

<img width="725" height="890" alt="image" src="https://github.com/user-attachments/assets/91136936-339b-4a67-9add-7688cfd5816c" />

<img width="737" height="600" alt="image" src="https://github.com/user-attachments/assets/76487f95-7f2b-43ae-a366-be510c6b0484" />

 

6. Wykonaj czynności z punktu 2-3 stosując je do folderu 
"SSO1". 
Tworzymy udział dla nowego folderu 

<img width="980" height="712" alt="image" src="https://github.com/user-attachments/assets/023447f4-047c-4254-8f30-780933dd8219" />

Dalej 

<img width="953" height="704" alt="image" src="https://github.com/user-attachments/assets/9afc67c1-93a6-48a2-a0bb-1488cb617643" />

<img width="954" height="690" alt="image" src="https://github.com/user-attachments/assets/4972fa17-b451-4853-85a3-74af14beffa2" />

<img width="943" height="688" alt="image" src="https://github.com/user-attachments/assets/fee41440-e1ac-472c-92d8-3650a729ba84" />

<img width="955" height="731" alt="image" src="https://github.com/user-attachments/assets/fe13a058-86e2-4e20-86ce-e30a16bf46b2" />

 
Wyłączamy dziedziczenie  

<img width="953" height="696" alt="image" src="https://github.com/user-attachments/assets/9ace7fd0-ab53-4f8b-b982-dca495a29dae" />

<img width="961" height="639" alt="image" src="https://github.com/user-attachments/assets/0a5165f3-fb74-478b-afc2-4531f4e9f565" />

Klikamy następnie Dodaj  
wybierz podmiot zabezpieczeń 

<img width="1002" height="704" alt="image" src="https://github.com/user-attachments/assets/f86b97be-cf6b-4928-8d9a-819ab4428fab" />

wpisujemy Informatycy 

<img width="824" height="464" alt="image" src="https://github.com/user-attachments/assets/10b30207-8d16-4512-a70f-ea5637f129a7" />

dodajemy pełnę kontrolę 

<img width="967" height="610" alt="image" src="https://github.com/user-attachments/assets/1c5afd47-bee8-4559-ab74-d1a7c58c7b90" />

Widzimy że Informatycy mają pełną kontrolę 

<img width="973" height="678" alt="image" src="https://github.com/user-attachments/assets/20ff9407-7a44-4420-84d1-1aa775a26eea" />

kończymy kreację 

<img width="978" height="665" alt="image" src="https://github.com/user-attachments/assets/ffd3b3fb-fc69-47b4-9810-b6829f3e2d01" />

<img width="962" height="691" alt="image" src="https://github.com/user-attachments/assets/93c527a1-6197-4dfc-bb77-f4108624ae7d" />

przydzielamy tak samo 100MB 

<img width="1026" height="523" alt="image" src="https://github.com/user-attachments/assets/4b0bc39c-ade8-4b56-aca3-ac4f1b9e2b77" />

ustawiamy też limit dla 5 użytkowników 

<img width="936" height="989" alt="image" src="https://github.com/user-attachments/assets/b2e6ef91-447c-4470-a921-4dac4776f60f" />


<img width="967" height="647" alt="image" src="https://github.com/user-attachments/assets/a9784d3e-fdd4-4280-adcc-091c5d834714" />


7. Utwórz dwie grupy: "Informatycy" i "Elektronicy". 
Tworzymy grupę Informatycy oraz Elektronicy w tym samym miejscu co użytkowników 
PPM i dodaj grupę

<img width="1004" height="591" alt="image" src="https://github.com/user-attachments/assets/cbc8c525-200f-4f5e-95eb-994fde2418e8" />

<img width="845" height="606" alt="image" src="https://github.com/user-attachments/assets/6631de0b-3603-4925-958a-9bf27b65e9eb" />
 
<img width="892" height="683" alt="image" src="https://github.com/user-attachments/assets/3240b7cc-78dc-4348-9074-3e7632c1e093" />

 
 
 
 
 
 
8. Przypisz użytkowników do tych grup, tak aby trzech z nich miało pełną kontrolę do obydwu folderów, a trzech pozostałych  pełną kontrolę do folderu "SSO", a do "SSO2" brak dostępu.

   
Informatycy będą mieli pełną kontrolę do obu folderów a elektronicy pełną kontrolę do sso1 i 
brak dostępu do sso2  
teraz dodajemy użytkowników do grup 
do grupy informatycy przejdą dariusz.kubica, adam.kwita i gniewomir.wielki 
do grupy elektornicy zostaną przydzieleni bastian.smok, andrzej.karcz i patryk.madej 
klikamy prawym przyciskiem myszy na każdego użytkownika i wpisujemy nazwę grupy do 
której chcemy go dodać 

<img width="626" height="621" alt="image" src="https://github.com/user-attachments/assets/cdb88139-8846-4cf1-bd6e-a8671f5377c7" />

<img width="759" height="393" alt="image" src="https://github.com/user-attachments/assets/94c793d0-a555-42e1-ac3b-e0365a783cdb" />

będzie pojawiac się takie okienko potwierdzające 

<img width="994" height="449" alt="image" src="https://github.com/user-attachments/assets/bc7d664a-ddc9-4d4d-8dc9-77a2251562b2" />

takie są skutki 

<img width="772" height="770" alt="image" src="https://github.com/user-attachments/assets/22fe493d-027f-4ebf-924e-811e68411646" />

<img width="826" height="826" alt="image" src="https://github.com/user-attachments/assets/601a012f-35dd-445e-83ff-820fbef39929" />

teraz przydzielimy uprawnienia do sso1 
klikamy ppm i właściwości 

<img width="937" height="597" alt="image" src="https://github.com/user-attachments/assets/ac6917c6-6d46-49d0-9e05-d9b16ff48cda" />

przechodzimy do zakładki uprawnienia i klikamy Dostosowywanie uprawnień 
pojawia się znany nam panel 

<img width="939" height="851" alt="image" src="https://github.com/user-attachments/assets/151ade4d-22ab-46a5-9f68-27dc6c9c0313" />

klikamy teraz usuń przy dariuszu kubicy 

<img width="972" height="623" alt="image" src="https://github.com/user-attachments/assets/e00ab912-4ac3-4316-8848-ca549937dae3" />

i dodajemy pełną kontrolę dla obu grup 

<img width="877" height="550" alt="image" src="https://github.com/user-attachments/assets/5e31fd88-6b1c-4b76-9a9b-8a96dd982fd3" />

klikamy zastosuj 
 
<img width="976" height="633" alt="image" src="https://github.com/user-attachments/assets/9ad26d42-0b5d-4142-a02e-e744e8550efd" />

 
 
teraz sprawdźmy na klientach czy zmiany  
 
logujemy się na gniewomira 
 
<img width="951" height="562" alt="image" src="https://github.com/user-attachments/assets/f297272c-216e-477a-87a3-151aff7e92d6" />

 
 
należy on do grupy informatycy więc powinien mieć pełny dostęp do obu folderów 
w sso1 utworzył nowy dokument tekstowy 

<img width="937" height="706" alt="image" src="https://github.com/user-attachments/assets/0bf9fce5-11a8-480d-b007-dc72c99e9a6a" />

widzimy że ma on pełną kontrolę nad oboma folderami 

<img width="946" height="905" alt="image" src="https://github.com/user-attachments/assets/17c5920d-3586-4d17-add6-2d1dbaf73ef6" />

<img width="946" height="717" alt="image" src="https://github.com/user-attachments/assets/16f47498-8c54-4e0e-8e75-2ec988d152f4" />



teraz sprawdźmy możliwości patryka madeja, który należy do grupy elektronicy 

<img width="939" height="690" alt="image" src="https://github.com/user-attachments/assets/ab8ad223-6df4-4d39-aa8c-5a2d54209d38" />

udało mu się otworzyć folder sso1 

<img width="939" height="704" alt="image" src="https://github.com/user-attachments/assets/1e979f2f-9cf2-44c1-9a91-2dbb82846039" />


do folderu sso2 jednak nie ma uprawnień więc wszystko się zgadza 

<img width="946" height="711" alt="image" src="https://github.com/user-attachments/assets/6614e513-4cfe-41ae-adf4-d4ddbe0dfe71" />

9. Utwórz jeden ukryty folder o dowolnej nazwie z prawami 
odczytu tylko dla użytkowników tych dwóch grup. 

W poradniku został pokazany sposób tworzenia ukrytych folderów i jak one działają  
tworzymy nowy udział 

<img width="968" height="669" alt="image" src="https://github.com/user-attachments/assets/a173fbe6-c035-414d-8a6f-45b76399a398" />

<img width="866" height="671" alt="image" src="https://github.com/user-attachments/assets/b46e14be-cdc4-4da1-91b2-aef490512cad" />

lokalizacja to d:\tajny$ 
 
<img width="980" height="647" alt="image" src="https://github.com/user-attachments/assets/b55e2f5c-c0ad-4499-b778-89deddafcfa7" />

tworzymy ten folder 

 <img width="959" height="686" alt="image" src="https://github.com/user-attachments/assets/41267d61-c341-4521-a0d9-337dffb1b2b2" />

 
 
Wybieramy Dostosowywanie uprawnień 

<img width="936" height="667" alt="image" src="https://github.com/user-attachments/assets/12243a83-155e-4092-a46f-5fb3d538274e" />

dodajemy Informatycy 

<img width="981" height="430" alt="image" src="https://github.com/user-attachments/assets/f7c6ee14-5766-41c5-a171-8e0b665148c9" />

oraz dodajemy  

<img width="834" height="815" alt="image" src="https://github.com/user-attachments/assets/00b9becb-887a-4daa-8f18-85dc1b403c72" />

elektornicy tylko do odczytu 
klikamy OK a następnie zakończ 

<img width="803" height="862" alt="image" src="https://github.com/user-attachments/assets/f56a009f-8414-4d80-bda5-96eb67289d5d" />

<img width="951" height="680" alt="image" src="https://github.com/user-attachments/assets/db142517-8ac9-4679-a5dd-3327148fe9d4" />

<img width="943" height="739" alt="image" src="https://github.com/user-attachments/assets/a9309857-d40c-4b66-a83f-0b5f62dc1a9c" />

z klienta możemy odczytać folder 

<img width="938" height="693" alt="image" src="https://github.com/user-attachments/assets/a2afc6cf-c65e-40b5-9723-81bd4ce35cee" />
 
 
 
podczas próby utworzenia pliku tekstowego pojawiło się takie okno, które potwierdza że jest 
możliwy tylko odczyt 

 <img width="971" height="554" alt="image" src="https://github.com/user-attachments/assets/849bff7b-2ef6-4021-a467-4a694123796d" />

 
 
oczywiście folder nie wyświetla się w tym miejscu 

<img width="955" height="689" alt="image" src="https://github.com/user-attachments/assets/182871aa-5e05-48c1-9789-f0e17bb1f03c" />

