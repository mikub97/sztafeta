# Sztafeta na Szczyt

Jednoplikowa gra diagnostyczna z matematyki (egzamin ósmoklasisty) do rozegrania
na jednym komputerze przez dwoje uczniów naraz. Statyczny HTML/CSS/JS, bez
backendu i bez zależności poza czcionkami z Google Fonts.

Dwa tryby do wyboru na starcie: drużynowy (wspólny wynik, bez porównywania
graczy) i rywalizacyjny (dwie osobne ścieżki). Te same 20 pytań w obu trybach,
w wersjach liczbowych A/B dla każdego z graczy — pokrywają moduły z
`../korepetycje/content/mat-e8.yaml` (ułamki, potęgi, procenty, równania,
proporcje, geometria, Pitagoras, pole figury, średnia/mediana, zadanie tekstowe).
Po grze — dwie zagadki bonusowe do rozwiązania wspólnie.

## Uruchomienie lokalnie

Wystarczy otworzyć `index.html` w przeglądarce — nie trzeba serwera.

## Publikacja na GitHub Pages

Najprościej jako osobne repo:

```bash
cd sztafeta-na-szczyt
git init
git add index.html README.md
git commit -m "Sztafeta na Szczyt — gra diagnostyczna mat-e8"
git branch -M main
git remote add origin git@github.com:mikub97/sztafeta-na-szczyt.git
git push -u origin main
```

Potem w ustawieniach repo (Settings → Pages) ustaw źródło na gałąź `main`,
katalog `/ (root)`. Strona wyląduje pod
`https://mikub97.github.io/sztafeta-na-szczyt/`.

Alternatywnie: skopiuj `index.html` do podkatalogu w `mikub97.github.io`
(np. `mikub97.github.io/sztafeta/index.html`), jeśli wolisz trzymać to jako
podstronę głównego repo zamiast osobnego.

## Dane uczniów

Strona nie zapisuje i nie wysyła nigdzie imion ani wyników — jedyny zapis to
`localStorage` w przeglądarce ucznia/nauczyciela, żeby przeżyło przypadkowe
odświeżenie strony w trakcie lekcji. Nic nie trafia do `data/korepetycje.db`
automatycznie — notatki z panelu „dla prowadzącego” trzeba przepisać ręcznie,
jeśli mają zostać przy uczniu.
