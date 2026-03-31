<img width="935" height="645" alt="image" src="https://github.com/user-attachments/assets/4634dc5d-a029-4ae9-8628-41533d7e50bc" /># Serwer plików SMB w W2012R2 #

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
Aby zobaczyć czy serwer DNS został skonfigurowany poprawnie przechodzimy do sekcji 
DNS 
klikamy prawym przyciskiem  SERWER i uruchamiamy Menedżer DNS 
W menedżerze przechodzimy  serwer.egzamin.zse>Strefy wyszukiwania do 
przodu>egzamin.local 
Widzimy że obie karty sieciowe są podłączone 
można sprawdzić to też we Właściwościach serwer.egzamin.zse 
Instalacja i Konfiguracja DHCP 
Teraz instalujemy trzecią rolę tym samym sposobem co poprzednie 
wybieramy serwer 
wybieramy funkcję serwer DHCP 
klikamy Dodaj funkcję  
a następnie przechodzimy Dalej 
nie instalujemy dodatkowych funkcji
Klikamy zainstaluj  
instalacja powiodła się  
przechodzimy do powiadomień 
tym razem dokończymy jednak konfigurację innym sposobem 
w narzędziach wybieramy DHCP 
rozwijamy teraz serwer.so.local 
na serwer egzamin.local klikamy prawym przyciskiem i włączamy autoryzację 
po rozwinięciu serwera pojawiły się protokoły IPv4 i IPv6 
IPv6 nie będzie potrzebne w naszej domenie, więc konfigurujemy jedynie IPv4\ 
Pojawiają się informacje o tym jak skonfigurować serwer DHCP 
klikamy na IPv4 prawym przyciskiem  i wybieramy nowy zakres 
Uruchomi się kreator nowych zakresów 
W nazwie najlepiej podać nazwę domeny  
posiłkując się topologią wiemy, że początkowy adres IP powinien wynosić 10.0.0.11, 
końcowy można ustawić jako np 10.0.0.199 
Długość to okres, po którym adresy ulegają zmianie  
Maskę podsieci ustawiamy na 255.255.255.0 ponieważ 255.0.0.0 mieści za dużo hostów 
Przechodzimy Dalej 
Teraz będziemy  tworzyć wykluczenia, czyli adresy, których nie przydziela serwer, tylko są 
one przydzielane ręcznie  
W tej sieci są to dwie drukarki 
Są to pojedyncze adresy dlatego wpisujemy je na początku i na końcu adresu 
Przechodzimy dalej. Można w tym miejscu zmienić czas dzierżawy, ale tego nie będziemy 
robić 
Potwierdzamy i przechodzimy Dalej 
Podajemy bramę domeny czyli najniższy adres z puli 
Przechodzimy dalej 
ustawiamy nazwę serwera “serwer” 
Adres IP ustawiamy na 10.0.0.1 i klikamy dodaj 
Teraz widzimy obie karty sieciowe 
Klikamy dalej 
Możemy teraz skonfigurować serwer WINS.  
Tłumaczy on adresy w sieci lokalnej 
nie ma potrzeby konfigurowania go teraz więc klikamy dalej 
i przechodzimy Dalej 
Zakończ 
Pojawiła się nowa sekcja - Zakres 
Zamykamy wszystkie okna i uruchamiamy serwer ponownie 
Należy teraz chwilę poczekać 
W powiadomieniach nadal mamy informacje o dalszej konfiguracji DHCP 
klikamy Dokończ 
Określamy w jaki sposób będzie autoryzowany dostęp do serwera 
możemy to pominąć 
zamykamy  
Jeżeli DHCP zostało skonfigurowane poprawnie powinny pojawić się zielone strzałki przy 
adresach IPv4 i IPv6 
Instalacja SMB 
Przechodzimy do Menedżera serwera 
Klikamy Dodaj role i funkcje 
Instalacja oparta na rolach 
Wybieramy też oczywiście serwer 
Szukamy roli Usługi plików i magazynowania 
na razie zainstalowana jest 1 z 11 funkcji 
zaznaczamy te 3 funkcje 
 
 
 
przechodzimy dalej 
 
 
niczego innego już nie dodajemy 
klikamy zainstaluj 
trwa instalacja, po jej zakończeniu klikamy Zamknij 
przechodzimy do menedżera serwera i wybieramy Usługi plików i magazynowania 
Przechodzimy do sekcji udziały 
rozwijamy Zadania i wybieramy nowy udział 
 
 
wybieramy szybkie SMB 
 
 
tworzymy ścieżkę na dysku D i nazywamy ją zasoby 
klikamy OK 
zezwalamy na drugą opcję i przechodzimy dalej  
teraz przydzielimy uprawnienia jednemu z użytkowników 
klikamy dostosowywanie uprawnień 
a następnie dodaj 
Następnie hiperłącze Wybierz podmiot zabezpieczeń 
pojawia się takie okno 
możemy od razu wpisać nazwę użytkownika bądź też wybrać go zaawansowanym 
sposobem 
Klikamy Znajdź teraz 
 
 
pojawiła się lista użytkowników 
 
 
Wybieramy na przykład użytkownika Piotr Jajo 
klikamy OK 
w polu do wpisania pojawiła się nazwa obiektu  
nadajemy tylko prawo odczytu i klikamy OK 
teraz usuwamy wpisy odnośnie innych grup/używkowników 
zaznaczamy interesujący nas wpis i klikamy Wyłącz dziedziczenie 
chcemy usuąć wszystkie uprawnienia 
dodajemy jeszcze administratora z pełną kontrolą 

klikamy zastosuj i OK 
przechodzimy dalej 
pojawia się takie podsumowanie  
jeżeli wszystko się zgadza klikamy Utwórz 
’ 
gdy się uda klikamy Zamknij  
w menedżerze serwera pojawił się dodany folder 
klikamy prawym przyciskiem myszy i wybieramy Konfiguruj przydział 
wybieramy 1000 MB i klikamy OK 
widizmy że przydzielone jest teraz 100 MB 
Sprawdźmy teraz działanie serwera na maszynie klienckiej  
Logujemy się na konto Piotr Jajo 
przechodzimy do eksploratora 
i wpisujemy tam \\serwer\zasoby 
gdy administrator doda aplikację do tego folderu użytkownik piotr jajo nie będzie mógł go 
uruchomić ponieważ ma tylko prawo do odczytu 
natomiast gdy dodamy tam plik tekstowy możemy go otworzyć bez problemu 
aby ułatwić otwieranie tego folderu możemy skorzystać z opcji mapuj dysk sieciowy  
Wybieramy literę dysku (np. Z) wpisujemy \\serwer\udział  i klikamy Zakończ 
Folder pojawił się jako dysk Z 
folderem możemy zarządzać też z innego miejsca 
Na serwerze uruchamiamy Narzędzia administracyjne a następnie Zarządzanie komputerem 
widzimy w odpowiedniej zakładce nasz folder 
widzimy że występują też ukryte foldery oznaczone znakiem dolara 
spróbujemy teraz utworzyć taki folder 
klikamy PPM i wybieramy Nowy udział 
przechodzimy dalej 
wpisujemy d:\ukryty$ i przechodzimy Dalej 
oczywiście jeżeli nie mamy takiej ścieżki to tworzymy ją w tej chwili 
klikamy Dalej 
i Zakończ 
pojawi się jeszcze podsumowanie  
klikamy jeszcze raz zakończ 
pojawił się nowo dodany folder  
folder nie pokazuje się gdy przejdziemy do zasobów sieciowych 
możemy jednak go otworzyć wpisując bezpośrednio jego lokalizację czyli \\serwer\ukryty$ 
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
