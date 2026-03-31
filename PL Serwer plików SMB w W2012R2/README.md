Tutoriale 
Instalacja i Konfiguracja AD i DNS 
Przechodzimy do menedżera serwera i klikamy dodaj role i funkcje 
Pojawi się strona informująca nas do czego służy ten kreator 
przechodzimy dalej 
Wybieramy czy instalacja ma być oparta na rolach czy usługach pulpitu zdalnego 
Zaznaczamy tutaj instalację opartą na rolach. Instalacja usług pulpitu zdalnego polega na 
instalowaniu funkcji na innych urządzeniach. 
 
 
Wybieramy na jakim serwerze mają zostać zainstalowane role 
 
 
pojawia się lista ról, które możemy zainstalwoać 
Wybieramy usługi domenowe Active Directory 
Klikamy Dodaj funkcje 
a następnie dalej 
nie instalujemy żadnych dodatkowych funkcji dlatego klikamy Dalej 
Dalej 
pojawia się potwierdzenie i klikamy zainstaluj 
 
 
instalacja przebiegła pomyślnie  
 
 
teraz wymagana jest konfiguracja  
Na pulpicie nawigacyjnym pojawił się kafelek nowej usługi 
pojawiło się też nowe narzędzie 
mamy też dostępną nową sekcję w ustawieniach 
pojawiło się powiadomienie że wymagana jest konfiguracja usług domenowych 
Klikamy w napis Podnieś poziom tego serwera… 
Pojawiła się  konfiguracja wdrażania  
Na początku wybieramy czy chcemy dołączyć  do istniejącej domeny czy stworzyć nową.  
Nie mamy jednak do dyspozycji żadnej istniejącej domeny. Stworzymy więc nową. Dodamy 
ją do nowego lasu domen, czyli grupy. 
Domenę nazywam egzamin.zse 
klikam dalej  
teraz przechodzimy do opcji kontrolera domeny 
na samej górze wybieramy poziom funkcjonalności lasu, czyli jakie systemy mogą obsłużyć 
pełnię jej funkcji 
na razie zostawiamy windows server 2012 
Serwer DNS pozostawiamy zaznaczony  
teraz musimy podać hasło trybu przywracania usług katalogowych. 
użytkownik który ma takie uprawnienia może uzyskiwać dostęp do danych na temat 
funkcjonalności serwera.Koliber123 
Hasło powinno być inne niż hasło głównego administratora. 
Będzie to w tym przypadku Koliber321 
przechodzimy Dalej  
pojawi się komunikat o niemożności utworzenia delegowania dla serwera DNS 
Delegowanie to wysyłanie odpowiedzi na żądanie od komputerów klienckich 
Klikamy dalej  
Teraz jest sprawdzane czy domena nie jest już wykorzystywana. 
nazwa domeny jest w porządku więc klikamy Dalej 
W tym miejscu konfigurujemy foldery dla usług katalogowych, czyli dla danych o 
funkcjonowaniu serwera. 
Pozostawiamy je domyślnie jeżeli mamy jeden serwer 
Przenosi nas do podsumowania 
klikamy dalej 
przenosi nas do weryfikacji konfiguracji 
w rozbudowanych sieciach może to potrwać bardzo długo, ale w małej sieci przebiegnie ona 
szybko 
klikamy zainstaluj 
Po instalacji nastąpi ponowne uruchomienie  
podczas logowania zauważamy że przed nazwą Administrator pojawiła się nazwa domeny 
Po zalogowaniu widzimy, że pojawiły się teraz dwa nowe kafelki 
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
