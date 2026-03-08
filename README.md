# 📁 Przestrzeń: Przemyślenia & Linki

> Centralna baza wiedzy i linków — dla Ciebie i dla Manus AI.
> Ostatnia aktualizacja: **2026-03-04** | Wersja: **2.0**

---

## Co tu znajdziesz

Ten folder to Twoja osobista baza linków z różnych źródeł — rozmów AI, artykułów, przemyśleń, projektów. Istnieje w trzech formatach, żeby zarówno Ty, jak i Manus AI mogli z niej korzystać w najwygodniejszy sposób.

| Plik | Format | Przeznaczenie | Jak używać |
|------|--------|--------------|------------|
| `index.html` | Mini strona HTML | Wizualna baza z wyszukiwarką | Pobierz i otwórz w przeglądarce |
| `LINKI.md` | Markdown | Główny plik dla Manusa | Edytuj bezpośrednio w Drive lub notatniku |
| `baza_linkow.csv` | Arkusz CSV | Dane strukturalne | Otwórz w Google Sheets |

---

## Jak dodawać linki

### Metoda 1 — Mini strona HTML (najwygodniejsza)

Pobierz plik `index.html` na komputer i otwórz w przeglądarce. Kliknij **+ Dodaj link**, wypełnij formularz. Dane zapisują się automatycznie w przeglądarce (`localStorage`). Użyj **Eksportuj JSON**, żeby zapisać kopię i wgrać ją z powrotem na Drive.

**Skróty klawiszowe:**
- `Ctrl+K` — otwórz wyszukiwarkę
- `Ctrl+Enter` — zapisz formularz
- `Esc` — zamknij modal / dialog

### Metoda 2 — LINKI.md (dla Manusa)

Otwórz plik `LINKI.md` w Google Docs lub dowolnym edytorze Markdown. Dodaj wiersz do odpowiedniej tabeli według schematu:

```
| [Tytuł](URL) | Opis co to jest i dlaczego ważne | #tag1 #tag2 | 2026-03-04 |
```

### Metoda 3 — CSV w Google Sheets

Otwórz `baza_linkow.csv` w Google Sheets (Plik → Importuj). Dodawaj wiersze ręcznie. Kolumny: `URL, Tytuł, Opis, Kategoria, Tagi, Data, Źródło, Priorytet`.

---

## Kategorie

| Ikona | Kategoria | Kiedy używać |
|-------|-----------|-------------|
| 💬 | Rozmowy AI | Linki do konkretnych sesji z ChatGPT, Claude, Manus |
| 🤖 | AI / Modele | Narzędzia AI, modele, platformy |
| 💼 | Biznes | Projekty, strategie, partnerzy, klienci |
| 💰 | Finanse | Inwestycje, kryptowaluty, raporty finansowe |
| ⚙️ | Tech / Dev | Kod, repozytoria, dokumentacja techniczna |
| 🔬 | Research | Artykuły, badania, raporty, wiedza |
| 🗂️ | Inne | Wszystko co nie pasuje gdzie indziej |

---

## Jak Manus korzysta z tej bazy

Kiedy poprosisz Manusa o dostęp do kontekstu lub powiesz "sprawdź moje linki", Manus:

1. Odczytuje plik `LINKI.md` z Google Drive
2. Wchodzi w linki oznaczone jako istotne
3. Analizuje treść i wyciąga wnioski
4. Uzupełnia swoje rozumienie Twojego kontekstu

**Najważniejsza sekcja dla Manusa** to `🧠 Profil i kontekst` w pliku `LINKI.md`. Uzupełnij ją raz, a Manus będzie rozumiał Cię bez pytania za każdym razem.

---

## Backup i synchronizacja

Dane w `index.html` przechowywane są w `localStorage` przeglądarki — **nie synchronizują się automatycznie z Drive**. Żeby nie stracić danych:

1. Regularnie klikaj **Eksportuj JSON** w mini stronie
2. Wgraj plik JSON na Drive (zastąp stary lub dodaj nowy)
3. Możesz też wgrać JSON z powrotem przez **Importuj JSON** — duplikaty są automatycznie pomijane

---

## Historia zmian

| Wersja | Data | Zmiany |
|--------|------|--------|
| 2.0 | 2026-03-04 | Naprawa XSS, edycja linków, potwierdzenie usuwania, eksport CSV, favicon, walidacja URL, `use strict`, ARIA |
| 1.0 | 2026-03-04 | Pierwsza wersja — mini strona HTML, LINKI.md, CSV |

---

*Prowadzone przez Manus AI dla właściciela konta.*
