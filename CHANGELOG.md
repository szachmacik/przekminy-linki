# 📋 CHANGELOG — Baza Linków Przekminy

> Historia wszystkich wersji i zmian. Prowadzona automatycznie przez Manus AI.

---

## [v5.0] — 2026-03-08 — Manus AI (autonomicznie)

### Dodano — HTML

- **Auto-fetch tytułu** — po wklejeniu URL automatycznie pobiera tytuł strony przez allorigins proxy (bez CORS); spinner podczas ładowania
- **Wyszukiwanie zaawansowane** — składnia `tag:ai`, `priorytet:wysoki`, `kategoria:tech`, `domena:github.com`; można łączyć wiele warunków naraz
- **Auto-backup co 10 zmian** — 3 ostatnie wersje bazy w localStorage; przycisk "Przywróć backup" w sidebarze
- **Chmura tagów** — sidebar z tagami, rozmiar czcionki proporcjonalny do liczby użyć; kliknięcie filtruje
- **Filtry kombinowane** — kategoria + priorytet + tag + wyszukiwanie jednocześnie; pasek aktywnych filtrów z przyciskami X do usuwania
- Walidacja 29/29 funkcji JS ✓ | Nawiasy klamrowe 416/416 (diff: 0) ✓

### Dodano — Python

- **`batch_import.py`** — masowy import linków z TXT/CSV/JSON/HTML zakładek Chrome/Firefox; auto-kategoryzacja, wykrywanie duplikatów, raport MD
- **`weekly_report.py`** — tygodniowy raport Markdown z bazy: statystyki, kategorie, priorytety, domeny, tagi, sekcja dla Manusa

### Dodano — Excel

- **Excel v3.0** — 7 arkuszy: Dashboard (KPI, ostatnio dodane), Baza Linków (hyperlinki, walidacja, autofiltr), Statystyki (wykres słupkowy + kołowy), Timeline (historia po miesiącach), Domeny (analiza domen), Manus Context (formularz profilu), Instrukcja
- Formatowanie warunkowe dla priorytetów (Wysoki = czerwone tło, Niski = zielone)
- Listy rozwijalne dla Priorytet i Kategoria

---

## [v4.0] — 2026-03-07 — Manus AI (autonomicznie)

### Dodano — HTML

- **Bulk import** — wklejanie wielu URLi naraz (jeden na linię lub format `URL | Tytuł | Kategoria`)
- **Widok domen** — grupowanie linków według domeny z rozwijaniem/zwijaniem
- **Undo / Redo** — pełny stos cofania z `Ctrl+Z` / `Ctrl+Y` (do 50 operacji)
- **Historia zmian** — panel z listą ostatnich 100 operacji z datą
- **PWA Service Worker** — tryb offline, strona działa bez internetu po pierwszym załadowaniu
- **Drag & Drop** — przeciągnij plik JSON lub URL z przeglądarki na stronę
- **Panel szybkich notatek** — `Ctrl+Q`, zapisywane lokalnie, eksport do Markdown
- **Pasek undo** — pojawia się po usunięciu linku, 6 sekund na cofnięcie
- **Licznik wyników** — `X z Y` podczas wyszukiwania i filtrowania
- **Przycisk X** — szybkie czyszczenie pola wyszukiwania
- **Pasek postępu** — wizualny feedback przy ładowaniu
- **Nowe skróty**: `Ctrl+B` (bulk), `Ctrl+Q` (notatki), `Ctrl+Y` (redo), `Ctrl+4` (domeny)

### Naprawiono — HTML

- Wszystkie linki jako natywne `<a href>` — eliminacja XSS
- `escHtml()` i `escAttr()` — pełna ochrona przed XSS w renderowaniu
- `'use strict'` na początku skryptu
- `try/catch` wokół wszystkich operacji `localStorage`
- `fallbackCopy()` dla przeglądarek bez Clipboard API
- Walidacja URL przez `new URL()` przed zapisem
- Wykrywanie duplikatów URL (w tym podczas bulk import)
- Pełne nagłówki sekcji w kodzie JS

### Dodano — Python

- **`link_health_checker.py`** — sprawdzanie dostępności linków (HEAD/GET, redirect detection, timeout, DNS errors, równoległe wątki, raport MD)
- **`manus_context_builder.py`** — auto-budowanie `MANUS_CONTEXT.md` z analizy bazy linków i profilu
- **`create_excel_v2.py`** — Excel v2.0 z 6 arkuszami, wykresami, walidacją, formatowaniem warunkowym

### Dodano — Excel

- Arkusz **Dashboard** z kartami KPI i rozkładem kategorii
- Arkusz **Statystyki** z wykresem słupkowym i kołowym
- Arkusz **Rozmowy AI** — dedykowany widok dla linków AI
- Arkusz **Do Zrobienia** — lista zadań z walidacją danych
- Arkusz **Instrukcja** — pełna dokumentacja
- Formatowanie warunkowe dla priorytetów
- Walidacja danych (listy rozwijalne) dla Priorytet i Status
- Hiperlinki w tytułach

### Dodano — Dokumentacja

- `CHANGELOG.md` — ten plik
- `ROADMAP.md` — plan rozwoju
- `MANUS_CONTEXT.md` — auto-generowany kontekst dla Manusa

---

## [v3.0] — 2026-03-05 — Manus AI (autonomicznie)

### Dodano — HTML

- Widok timeline (chronologiczny, grupowany po miesiącach)
- Panel statystyk na żywo (5 kart KPI)
- Tryb ciemny / jasny z persystencją
- Priorytety linków (Wysoki / Średni / Niski) z kolorowym paskiem
- Notatki prywatne do każdego linku
- Eksport Markdown
- Eksport CSV
- Auto-kategoryzacja po domenie (25+ reguł)
- Favicon z Google dla każdej domeny
- Klikalne tagi — filtrowanie jednym kliknięciem
- Filtr priorytetu w sidebarze
- Licznik wyników wyszukiwania
- Skróty klawiszowe rozszerzone (`Ctrl+T`, `Ctrl+1/2/3`)
- Panel skrótów klawiszowych (`?`)

### Naprawiono — HTML

- XSS: linki jako natywne `<a href>` (eliminacja `onclick="openLink()"`)
- `clipboard.writeText` z `catch` i fallback
- `'use strict'` na początku skryptu
- Walidacja URL przez `new URL()`
- Wykrywanie duplikatów URL
- Bezpieczny zapis z `try/catch`

### Dodano — Python

- `analyze_links.py` — auto-analiza linków, pobieranie tytułu, sugestia tagów, raport MD

### Dodano — Excel

- Arkusz Przegląd z kartami statystyk
- Arkusz Baza Linków z filtrowaniem
- Arkusz Statystyki z wykresem słupkowym
- Arkusz Instrukcja

---

## [v2.0] — 2026-03-05 — Manus AI

### Dodano

- Edycja linków (przycisk ✏️ na karcie)
- Potwierdzenie przed usunięciem (dialog z nazwą linku)
- Eksport CSV
- Favicon z Google dla domen
- Licznik wyników wyszukiwania
- Przycisk X w wyszukiwarce
- Wykrywanie duplikatów URL
- `Ctrl+Enter` do zapisania formularza
- Animacja modala `slideUp`
- Bezpieczny zapis `try/catch` wokół `localStorage.setItem`
- `'use strict'`

### Naprawiono

- XSS w `onclick` — eliminacja `onclick="openLink('${url}')"` 
- Brak obsługi błędu `clipboard.writeText`
- Brak walidacji URL
- Urwany komentarz sekcji JS
- Brak ARIA atrybutów

---

## [v1.0] — 2026-03-04 — Manus AI

### Pierwsze wydanie

- Mini strona HTML z kartami linków
- Wyszukiwarka z `Ctrl+K`
- Kategorie w sidebarze
- Dodawanie linków z opisem, tagami i kategorią
- Eksport / import JSON
- Tryb ciemny
- Plik LINKI.md dla Manusa
- Plik CSV
- README.md

---

*Changelog prowadzony przez Manus AI | Ostatnia aktualizacja: 2026-03-06*
