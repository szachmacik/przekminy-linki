# 🗺 ROADMAP — Baza Linków Przekminy

> Plan rozwoju na kolejne wersje. Aktualizowany przez Manus AI.
> Wszystkie pozycje oznaczone ✅ nie wymagają Twoich kluczy/dostępów — Manus może je wdrożyć autonomicznie.
> Pozycje oznaczone 🔑 wymagają zewnętrznych kluczy lub uprawnień.

---

## ✅ v5.0 — UKOŃCZONE (2026-03-08)

| Funkcja | Status |
|---------|--------|
| Auto-fetch tytułu strony | ✅ |
| Wyszukiwanie zaawansowane `tag:ai priorytet:wysoki` | ✅ |
| Auto-backup co 10 zmian (3 wersje) | ✅ |
| Chmura tagów w sidebarze | ✅ |
| Filtry kombinowane z paskiem aktywnych | ✅ |
| batch_import.py (TXT/CSV/JSON/HTML zakładki) | ✅ |
| weekly_report.py (raport tygodniowy) | ✅ |
| Excel v3.0 (7 arkuszy, wykresy, dashboard) | ✅ |

---

## v6.0 — Następna wersja autonomiczna (gotowe do wdrożenia)

Wszystkie poniższe funkcje mogą zostać zaimplementowane przez Manusa bez żadnych dodatkowych uprawnień.

| Funkcja | Opis | Priorytet |

Wszystkie poniższe funkcje mogą zostać zaimplementowane przez Manusa bez żadnych dodatkowych uprawnień.

| Funkcja | Opis | Priorytet |
|---------|------|-----------|
| Podgląd strony (screenshot.guru) | Hover → miniaturka strony, publiczne API bez klucza | Wysoki |
| Inteligentne sugestie tagów | Analiza tytułu+domeny → propozycja 3–5 tagów przy dodawaniu | Wysoki |
| Grupowanie po projekcie | Nowe pole "Projekt" — filtrowanie i widok per-projekt | Wysoki |
| Sortowanie drag & drop kart | Zmiana kolejności kart przez przeciąganie | Średni |
| Tryb prezentacji | Pełnoekranowy widok bez sidebarów | Średni |
| Skróty kontekstowe | `Ctrl+C` kopiuje URL karty, `Ctrl+E` otwiera edycję | Średni |
| Motywy kolorystyczne | 3 motywy: Dark, Light, Midnight Blue | Niski |
| Licznik kliknięć | Sortowanie po popularności linków | Niski |
| Archiwizacja | Przenoszenie do archiwum zamiast usuwania | Niski |

---

## v5.0 — Wersja z integracjami (wymaga kluczy API)

| Funkcja | Opis | Wymaga |
|---------|------|--------|
| 🔑 Auto-fetch metadanych | Pobieranie tytułu, opisu, obrazka OG przez własne API | Serwer lub Supabase Edge Function |
| 🔑 Synchronizacja z Google Sheets | Automatyczna synchronizacja bazy z arkuszem | Google API |
| 🔑 AI auto-kategoryzacja | GPT-4 analizuje URL i sugeruje kategorię, tagi, opis | OpenAI API |
| 🔑 AI podsumowanie rozmów | Wchodzi w link do rozmowy AI i generuje podsumowanie | OpenAI API + dostęp do URL |
| 🔑 Powiadomienia o martwych linkach | Cron job sprawdzający dostępność co tydzień | Serwer lub Supabase |
| 🔑 Udostępnianie kolekcji | Publiczny link do wybranej kategorii linków | Supabase lub hosting |
| 🔑 Import z przeglądarki | Importuj zakładki z Chrome/Firefox (plik HTML) | Plik zakładek |
| 🔑 Integracja z Notion | Synchronizacja z bazą danych Notion | Notion API |
| 🔑 Integracja z Raindrop.io | Import/eksport z Raindrop | Raindrop API |
| 🔑 Mobilna wersja PWA | Instalowalna aplikacja na telefon | Serwer HTTPS |

---

## v6.0 — Wersja aplikacji webowej

Pełna aplikacja webowa z backendem (Supabase + Vercel) z:

| Funkcja | Opis |
|---------|------|
| 🔑 Konta użytkowników | Logowanie, synchronizacja między urządzeniami |
| 🔑 Baza danych w chmurze | Supabase PostgreSQL — nie localStorage |
| 🔑 Rozszerzenie do przeglądarki | Dodawanie linków jednym kliknięciem |
| 🔑 API REST | Programowy dostęp do bazy linków |
| 🔑 Webhooks | Powiadomienia przy dodaniu linku |
| 🔑 Wersjonowanie linków | Historia zmian każdego linku |
| 🔑 Kolaboracja | Współdzielona baza z innymi użytkownikami |

---

## Zrealizowane (historia)

| Wersja | Data | Kluczowe funkcje |
|--------|------|-----------------|
| v1.0 | 2026-03-04 | Pierwsze wydanie, karty, wyszukiwarka, JSON |
| v2.0 | 2026-03-05 | Edycja, potwierdzenie usunięcia, CSV, favicon |
| v3.0 | 2026-03-05 | Timeline, statystyki, tryb ciemny/jasny, priorytety, auto-kategoryzacja |
| v4.0 | 2026-03-06 | Bulk import, domeny, undo/redo, historia, PWA, drag&drop, szybkie notatki |

---

## Priorytety dla Manusa — co wdrożyć następnym razem (v6.0)

Gdy powiesz "rozbuduj dalej", Manus zacznie od tych pozycji (wszystkie autonomiczne):

1. **Podgląd strony** — miniaturka przy hover, screenshot.guru API (publiczne, bez klucza)
2. **Sugestie tagów** — auto-propozycja na podstawie tytułu i domeny
3. **Grupowanie po projekcie** — nowe pole Projekt, widok per-projekt
4. **Sortowanie drag & drop** — zmiana kolejności kart
5. **Skróty kontekstowe** — Ctrl+C/E na kartach

---

*Roadmap prowadzony przez Manus AI | Ostatnia aktualizacja: 2026-03-08*
