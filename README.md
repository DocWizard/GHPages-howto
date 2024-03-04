# Jak opublikować output z MadCap Flare w GitHub Pages.

## Wersja z integracją MCF z GitHubem. 
[Tu dostępny wariant łatwiejszy, wykorzystujący GitHub Desktop](./README2.md)

## Krok 1 - Jeśli nie mamy jeszcze zainstalowanego Gita - należy ściągnąć i zainstalować - [LINK](https://git-scm.com/downloads). Uwaga! GitHub Desktop to nie to samo, co Git! 

## Krok 2 - Łączymy projekt z repo w GitHubie. [Tu jest doskonała dokumentacja (LINK)](https://docsy-site.netlify.app/docs/madcap-flare/connect-madcap-to-git/#bind-using-the-flare-interface)

> [!CAUTION]
> Przechodzimy przez wszystkie kroki z powyższego tutoriala do punktu 'Upload your Madcap project to GitHub using VS Code'. Nie ma potrzeby łączenia VS Code z GitHubem!

> [!CAUTION]
> Powyższy tutorial nie uwzględnia momentu, w którym MCF prosi o login i hasło do GitHuba. Gdy pojawi się takie okno dialogowe, należy podać te dane.

## Krok 3 - Przygotowanie projektu do publikacji w GitHub Pages:

### Najpierw przechodzimy przez poniższe kroki, by zmienić format outputu - zależy nam, by główna strona projektu nazywała się 'index.html':
<kbd>![alt text](./Resources/MCF.png)</kbd>

### Następnie tworzymy nowy publishing destination, przechodząc poniższe kroki:


<kbd>![alt text](./Resources/A1.png)</kbd>
<kbd>![alt text](./Resources/A2.png)</kbd>
> [!CAUTION] 
> Uwaga - w tym przypadku folder docelowy musi nazywać się 'Docs' i być w głównym katalogu repozytorium. Czyli jeśli repozytorium mamy w folderze C:\Github\Repozytorium, to folder docelowy ustawiamy jako C:\Github\Repozytorium\Docs.
>
<kbd>![alt text](./Resources/A3.png)</kbd>
<kbd>![alt text](./Resources/A4.png)</kbd>

Następnie z poziomu MCF możemy kliknąć PUBLISH. Output z naszą gotową stroną powinien wpaść do przed chwilą wybranego folderu.

Od tego momentu w menu "Source Control" (na samej górze, w pasku zadań) mamy też standardowe operacje Gitowe - commit, pull, push. W praktyce, do większości celów wystarczy nam opcja 'publish'.

<kbd>![alt text](./Resources/MCF2.png)</kbd>

## Krok 4 - Projekt gotowy do publikacji

W targecie HTML5 robimy Publish:

<kbd>![alt text](./Resources/publish.gif)</kbd>

Cały projekt powinien wpaść do naszego, utworzonego w kroku 2. repozytorium. Zaglądamy tam teraz, wchodząc na stronę repozytorium w serwisie GitHub.

>[!TIP]
>Warto sprawdzić dwie rzeczy:
> * Czy na pewno mój output HTML trafia do folderu Docs?
>
> * Czy na pewno w folderze Docs znajduje się plik index.html? 

##  Krok 5 - Co zrobić w GitHubie

Ustawiamy GitHub Pages:

<kbd>![alt text](./Resources/0.png)

Jeśli pojawią się błędy przy publikacji, możliwe że defaultowe ustawienia GitHub Pages nie radzą sobie z wybranym przez nas template. W takim wypadku ustawiamy jako source 'GitHub Actions', a nie 'Deploy from a Branch', wykonując poniższe kroki:

<kbd>![alt text](./Resources/B1.png)</kbd>

Następnie musimy wybrać odpowiedni workflow:

<kbd>![alt text](./Resources/1.png)</kbd>
<kbd>![alt text](./Resources/2.png)</kbd>
<kbd>![alt text](./Resources/3.png)</kbd>
<kbd>![alt text](./Resources/4.png)</kbd>
<kbd>![alt text](./Resources/5.png)</kbd>
<kbd>![alt text](./Resources/6.png)</kbd>
<kbd>![alt text](./Resources/7.png)</kbd>
<kbd>![alt text](./Resources/8.png)</kbd>

## Krok 6 - Finisz
Teraz, każdorazowo po wprowadzeniu w naszym projekcie w MCF zmian które chcemy opublikować na stronie, ponawiamy krok 4, czyli publish HTML5 output. Jeśli wszystko poszło zgodnie z planem, to za chwilę output powinien się pojawić na stronie.

<kbd>![alt text](./Resources/publish.gif)</kbd>