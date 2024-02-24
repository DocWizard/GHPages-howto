# Jak opublikować output z MadCap Flare w GitHub Pages.

## Krok 1A - Co zrobić w MCF:

![alt text](./Resources/MCF.png)

*Teoretycznie* to wystarczy. Teraz każdorazowo po wprowadzeniu zmian w projekcie możemy kopiować zawartość folderu ./Output/{user}/HTML5 do naszego gitowego repozytorium. Tracimy możliwość automatyzacji tego procesu, ale jeśli komuś bardzo zależy na czasie, albo — zwyczajnie po ludzku — mu się nie chce, to jest to możliwa opcja. W tym wypadku przechodzimy od razu do kroku 4.

## Krok 1B - Co zrobić w MCF: Wersja z integracją MCF z GitHubem. Robimy to, co wyżej, plus:

## Krok 2 - łączymy projekt z repo w GitHubie. [Tu jest doskonała dokumentacja (LINK)](https://docsy-site.netlify.app/docs/madcap-flare/connect-madcap-to-git/#bind-using-the-flare-interface)

## Krok 3 - gdy już mamy repozytorium, tworzymy nowy output destination:

![alt text](./Resources/A1.png)
![alt text](./Resources/A2.png)
![alt text](./Resources/A3.png)

> [!CAUTION] 
> Uwaga - folder docelowy musi nazywać się 'docs' i być w głównym katalogu  repozytorium. Czyli jeśli repozytorium mamy w folderze C:\Github\Repozytorium, to folder docelowy ustawiamy jako C:\Github\Repozytorium\docs.

![alt text](./Resources/A4.png)

##  Krok 4 - Co zrobić w GitHubie

Na tym etapie powinniśmy mieć stworzone repozytorium w GitHubie - albo z poziomu MCF, albo utworzone ręcznie (gdzie będziemy sami, ręcznie wkładać output).

>[!TIP]
>Warto sprawdzić dwie rzeczy:
>
> * Czy na pewno mój output HTML znajduje się w folderze Docs> (Nie dotyczy, jeśli wrzucamy pliki do repo ręcznie)
>
> * Czy na pewno w folderze Docs znajduje się plik index.html, a nie 'home.htm'? 

Gdy mamy już repozytorium z naszym outputem, otwieramy je z poziomu serwisu GitHub. Ustawiamy GitHub Pages - to powinniśmy już umieć. Settings -> Pages -> Deploy from a branch -> Branch MASTER / docs. 
![alt text](B1.png)

> [!NOTE]
> (Prawdopodobnie powinno działać też jeśli wybierzemy jako source 'GitHub Actions', ale przyznam, że jeszcze nie testowałem.)

Automatycznie uruchomi się build - niepotrzebnie, ale w niczym to nam nie przeszkadza. Github próbuje przerobić nasz output HTML przez generator stron statycznych, i niemal na pewno mu to nie wyjdzie. Musimy zmusić go, żeby potraktował nasz output jako gotową stronę. W tym celu klikamy po kolei:

![alt text](./Resources/1.png)
![alt text](./Resources/2.png)
![alt text](./Resources/3.png)
![alt text](./Resources/4.png)
![alt text](./Resources/5.png)
![alt text](./Resources/6.png)
![alt text](./Resources/7.png)
![alt text](./Resources/8.png)

Jeśli wszystko poszło zgodnie z planem, to za chwilę output powinien się pojawić w deployments.
