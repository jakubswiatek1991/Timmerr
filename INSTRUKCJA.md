# Minutnik PWA — instrukcja wdrożenia

## Struktura plików
```
minutnik/
├── index.html       ← główna aplikacja
├── manifest.json    ← manifest PWA
├── sw.js            ← service worker (offline)
├── INSTRUKCJA.md    ← ten plik
└── icons/
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-192.png
    ├── icon-512.png
    └── screenshot.png
```

---

## Krok 1 — GitHub Pages (darmowy hosting)

1. Wejdź na **github.com** i zaloguj się (lub załóż konto)
2. Kliknij **New repository** (zielony przycisk, prawy górny róg)
3. Nazwa repozytorium: `minutnik`
4. Zaznacz **Public**, kliknij **Create repository**
5. Kliknij **uploading an existing file**
6. Przeciągnij i upuść WSZYSTKIE pliki z tego folderu
   - Pamiętaj też o folderze `icons/` — wgraj wszystkie pliki z środka
7. Kliknij **Commit changes**
8. Idź do **Settings → Pages**
9. W sekcji "Source" wybierz branch **main**, folder **/ (root)**
10. Kliknij **Save**
11. Za ~2 minuty pojawi się link: `https://TWOJA_NAZWA.github.io/minutnik`

---

## Krok 2 — PWABuilder → plik AAB dla Google Play

1. Wejdź na **pwabuilder.com**
2. Wklej link z GitHub Pages i kliknij **Start**
3. Poczekaj na analizę (ok. 30 sekund)
4. Kliknij **Package for stores → Google Play**
5. Wypełnij dane: nazwa apki, opis, kategoria (Produktywność)
6. Pobierz plik `.zip` zawierający plik `.aab`

---

## Krok 3 — Google Play Console

1. Wejdź na **play.google.com/console**
2. Zapłać jednorazowo **25 USD** za konto dewelopera
3. Kliknij **Utwórz aplikację**
4. Wypełnij: tytuł, opis krótki i długi, kategoria, ocena treści
5. Wgraj plik `.aab` z PWABuilder
6. Dodaj minimum 2 zrzuty ekranu (możesz zrobić screenshot z przeglądarki)
7. Wypełnij kwestionariusz oceny treści
8. Kliknij **Opublikuj w wewnętrznym torze testowym** (najpierw)
9. Po testach → **Produkcja → Przejrzyj i opublikuj**
10. Czas weryfikacji Google: 1–3 dni robocze

---

## Sterowanie głosem (tylko Chrome/Android)

Sterowanie głosem wymaga HTTPS — GitHub Pages to zapewnia automatycznie.

### Domyślne komendy:
- **"start"** — uruchom timer
- **"stop"** — zatrzymaj timer
- **"reset"** — resetuj
- **"praca 25"** — ustaw czas pracy na 25 minut
- **"przerwa 5"** — ustaw czas przerwy na 5 minut

### Własne komendy:
Naciśnij mały biały przycisk mikrofonu przy każdym elemencie,
powiedz swoje słowo i kliknij "zapisz".
