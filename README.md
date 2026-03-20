
# 🎬 Mongoflix - Projekt Warstwy Danych

Witaj w zespole inżynierskim Mongoflix! 
Twoim zadaniem jest zaprojektowanie, wdrożenie i przetestowanie struktury bazy danych MongoDB dla nowej platformy streamingowej.

> **Status Projektu:** 🟡 W trakcie realizacji  
> **Stack Technologiczny:** MongoDB, JavaScript (ES6+)

---

## 📩 Wiadomość od Klienta (Brief Biznesowy)

*Poniżej znajduje się surowa notatka ze spotkania z zarządem. Twoim zadaniem jest przeanalizowanie tego tekstu i wyodrębnienie z niego wymagań technicznych.*

> "Słuchajcie, robimy Mongoflix i to musi być hit. Nie chcę sztywnych tabel jak w starych systemach. Każdy film w naszym systemie musi być opisany konkretnie: tytuł, data kiedy to weszło do kin, no i gatunki. Tylko nie ograniczajcie nas do jednego gatunku! Jak film jest komedią i horrorem naraz, to system musi to łyknąć. 
>
> Co do obsady, to wiecie jak jest – ludzie kochają gwiazdy. Chcemy widzieć kto reżyserował, ale też listę wszystkich aktorów, nawet jeśli jest ich dwudziestu. Skoro już o ludziach mowa, to nasi widzowie muszą mieć głos. Chcemy ocen (tak od 1 do 10) i krótkich recenzji pod filmami, żeby był ruch w interesie. Tylko pilnujcie porządku – nie chcemy, żeby jedna osoba psuła ranking i waliła dziesięć opinii pod jednym filmem. Jeden widz, jeden głos, jedna recenzja. Jasne?
>
> Zarabianie? Oczywiście. Niektóre filmy będą 'Premium' za kasę, inne 'Public' za darmo – musimy to jakoś odróżniać w bazie. I na koniec najważniejsze dla księgowości: musimy wiedzieć, ile razy dany film został odpalony. Od tego zależą tantiemy dla twórców, więc ten licznik musi działać bezbłędnie przy każdym obejrzeniu. Powodzenia!"

---


## 📂 Twoje Zadania

### 1. 📐 Modelowanie (`docs/schema.md`)
W folderze `docs` opisz strukturę dokumentu JSON.
* Jakie pola i typy danych wybierzesz?
* Czy opinie będą zagnieżdżone (embedded) czy w osobnej kolekcji?
* Jak zapewnisz unikalność opinii jednego użytkownika?

### 2. 🌱 Seedowanie Danych (`scripts/seed.js`)
Napisz skrypt JavaScript, który wykonasz w `mongosh`. Skrypt powinien:
* Przełączyć się na bazę `mongoflix`.
* Wyczyścić kolekcję `movies` (`db.movies.drop()`).
* Wstawić (`insertMany`) minimum **10 filmów** zgodnych z briefem.
* **Ważne:** Używaj `printjson()` lub `console.log()` do potwierdzenia, że dane zostały dodane.

### 3. 📊 Analityka (`queries/analysis.js`)
Napisz skrypt z zapytaniami agregującymi (`db.collection.aggregate([...])`).
* Znajdź filmy z kategorii "Action" po 2020 roku.
* Oblicz średnią ocen dla filmów.
* Policz łączną liczbę wyświetleń dla reżyserów.
* Użyj `printjson()`, aby wyświetlić wyniki w terminalu.

---

## ⚙️ Instrukcja Uruchomienia (Setup)

**Nie klonuj tego repozytorium bezpośrednio!** Nie będziesz mógł zapisać swojej pracy.
Aby rozpocząć projekt, wykonaj te kroki:

1.  Spójrz w prawy górny róg tej strony na GitHubie.
2.  Kliknij zielony przycisk **Use this template** -> **Create a new repository**.
3.  **Nazwij swoje repozytorium:** `mongoflix-nazwisko1-nazwisko2` (np. `mongoflix-kowalski-nowak`).
4.  Ustaw widoczność na **Public**.
5.  Dopiero teraz **sklonuj SWOJE nowe repozytorium** na komputer:
    ```bash
    git clone [https://github.com/TWOJ-LOGIN/mongoflix-nazwisko1-nazwisko2.git](https://github.com/TWOJ-LOGIN/mongoflix-nazwisko1-nazwisko2.git)
    ```

---

## 🛑 Zasady "Clean Code"

1.  **Nie commitujemy haseł!** Plik `.env` musi być w `.gitignore`.
2.  **Nazewnictwo:** Używaj języka angielskiego w kodzie (zmienne, funkcje).
3.  **Formatowanie:** Kod musi być czytelny. Użyj Prettiera lub innej wtyczki formatującej.

---
*Powodzenia, Zespół Mongoflix* 🚀

---
# 📋 Tablica kanban.

## :tools: Jak to zrobić na GitHubie?
- W repozytorium kliknij zakładkę Projects.
- Wybierz New project -> Board.
- GitHub sam stworzy kolumny: Todo, In Progress, Done. Możecie dodać kolumnę Testing pomiędzy nich.
- Dzięki temu Ty, wchodząc na ich projekt, od razu widzisz:
- Kto nic nie robi (pusta kolumna "In Progress").
- Kto utknął (zadanie wisi w "Testing" trzeci dzień).
- Ile realnie zostało do końca.

## Przykładowe zagadnienia na tablicę
:triangular_ruler: Etap 2: Projektowanie (Design)
[ ] Opracowanie struktury dokumentu filmu w pliku docs/schema.md.
[ ] Określenie typów danych dla pól (np. String, Int32, Date, Array).


:floppy_disk: Etap 3: Dane i Zasilanie (Data & Seeding)
[ ] Przygotowanie zestawu min. 10 dokumentów w formacie JSON (pliki data/movies.json).
[ ] Napisanie skryptu scripts/seed.js (czyszczenie bazy i insertMany).
[ ] Test zasilania bazy: Sprawdzenie czy dane poprawnie lądują w MongoDB.

:mag: Etap 4: Logika i Analiza (Implementation)
[ ] Napisanie zapytania wyszukującego filmy z konkretnego gatunku (find).
[ ] Napisanie zapytania filtrującego filmy po dacie i ocenie (operators: $gt, $and).
[ ] Stworzenie agregacji (aggregate): Średnia ocena dla każdego gatunku.
[ ] Napisanie skryptu aktualizującego dane (np. dodanie pola featured: true).

:checkered_flag: Etap 5: Finalizacja (Review & Delivery)
[ ] Weryfikacja kodu przez partnera (Code Review).
[ ] Uzupełnienie dokumentacji w README.md (instrukcja uruchomienia).
[ ] Finalny git push i sprawdzenie czy Webhook poprawnie zaraportował koniec prac.






