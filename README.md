* Przeznaczenie
  
Program służy do automatycznej edycji tekstowych plików .SRT tworzonych jako dodatek do plików video .MP4 lub .LRF. Zawierają one ważne informacje takie jak data, czas, wsþółrzędne geograficzne, pułap lotu, parametry czcionki itp.

Podstawową funkcjonalnością programu jest konwersja położeń geograficznych drona zapisanych w pliku .SRT na jego aktualny adres. Dodatkowymi, wyświetlanymi atrybutami są: aktualne położenie geograficzne, aktualna odległość drona w poziomie od miejsca rozpoczęcia nagrywania, oraz aktualny przelot drona, również od punktu rozpoczęcia nagrywania. Oprócz tego umożliwia on prostą edycję napisów. Tworzona jest równiez kopia oryginalnego pliku SRT. Ma ona rozszerzenie .SRT_copy.
Poniżej zamieszczony jest przykładowy kadr video.

![alt text](https://github.com/mbwasik/DronLocaliz_v2/blob/master/BD.png)

* Wymogi wstępne
     1) Komputer z systemem operacyjnym (OS) Windows 10, Windows 11 lub Linux np. dystrybucja Debian i dostępem do internetu. Na tychże OS program był testowany.
     2) Wskazana jest instalacja media playera vlc, np. ze strony https://www.videolan.org/vlc/ 

* Instalacja
     1) W systemie utworzyć dowolny \<Katalog\> (katalog o dowolnej nazwie)
     2) 
       - w systemie Windows do katalogu <Katalog> skopiować zawartość katalogu DystrybucjaWindows,
        czyli katalog _internal oraz plik DronLocalizWin_v2.exe
       - w systemie Linux do katalogu <Katalog> skopiować całą zawartość katalogu DystrybucjaLinux.
     3) Do katalogu \<Katalog\> skopiować z karty SD drona stosowne pliki MP4 i/lub LRF, oraz SRT.

* Uruchomienie
     1) Otworzyć okno terminala (w Windows 11 nacisnąć klawisz Windows i klawisz R (Win + R) lub np. kliknąć prawym przyciskiem myszy na menu Start i wybrać "Terminal") 
     2) Wykorzystując np. polecenie cd przejść do stosownego katalogu
     3) Uruchomić właściwy program:
     4) 
       - w Windows 11: wpisać DronLocalizWin_v2.exe -r True   i potwierdzić to przez <Enter>
         (DronLocalizWin.exe --h  pokazuje pomoc)
       - w Linuxie: > sudo DronLocalizLin_v2.bin -r True
         (DronLocalizLin_v2.bin --h  pokazuje pomoc)
     5) Odpowiedzieć na stosowne pytania (w nawiasach podane są wartości domyślne):

        a) wybrać plik SRT do przetwarzania  

        b) podać wielkość i kolor czcionki oraz rozmieszczenie napisów

        c) wpisać ewentualny dodatkowy napis, oraz jego wielkość i kolor

        d) ostatnią wielkością którą trzeba podać jest dokładność zaokrąglenia współrzędnych geograficznych, czyli ilość cyfr po    przecinku. Wartość ta jest o tyle istotna, że wpływa ona na dokładność określenia  adresu i czas wykonywania konwersji.               Im cyfra ta jest większa, tym dokładność określenia adresów jest również większa, ale częstotliwość zapytań internetowych także rośnie.
  Może to niekiedy powodować przeciążenie serwerów internetowych, które to wtedy zrywają połączenie. W              przypadku takim należy uruchomić program w innych godzinach lub zmniejszyć dokładność.
      
* Uwagi końcowe
  
     Do przeglądania nagrań video wykorzystywałem media playera VLC. Z innymi playerami bywa różnie, ale po umieszczniu napisów bezpośrednio w MP4 (też przy pomocy VLC), na pozostałych playerach też było OK.
     Można również umieścić napisy bezpośrednio w MP4. Nie jest już wtedy potrzebny plik SRT, a także MP4 z napisami uruchamia się bez problemów na innych przeglądarkach. Jak to zrobić? Tak skrótowo, w VLC:                                                  "Plik"--->"Konwertuj/Zapisz"--->"+Dodaj"(wybrać stosowny plik MP4)--->zaznaczyć "Użyj pliku z napisami"--->"Przegladaj"(wybrać stosowny plik SRT)--->"Konwertuj/Zapisz"--->"Przeglądaj"--->Wpisz dowolną nazwę nowego pliku MP4, koniecznie z rozszerzeniem MP4--->Save--->Start i chwilę odczekać na koniec "wtapiania".
