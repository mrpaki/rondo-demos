# rondo-demos

Showroom šablona za [rondo.rs](https://rondo.rs) — 10 demo landing stranica po delatnosti,
sa generičkim sadržajem na srpskom. Čist statički HTML/CSS/JS, bez build alata.

## Struktura

```
/
├── index.html              ← showcase stranica (lista svih demoa)
├── assets/
│   ├── base.css            ← zajednički design system (tokeni, layout, komponente)
│   └── base.js             ← mobilni meni, smooth scroll, scroll-reveal
├── medicinska/             ← Ordinacija Plus (#0ea5e9, centered hero)
├── stomatoloska/           ← Dental Studio (#06b6d4, photo hero)
├── auto-delovi/            ← AutoParts Centar (#f59e0b, dark split hero)
├── salon/                  ← Studio Bella (#e11d48, reversed split)
├── restoran/               ← Restoran Raskrsnica (#c2410c, warm photo)
├── advokat/                ← AK Đorđević (#1e3a8a, dark serif centered)
├── gradjevina/             ← Gradnja Pro (#eab308, dark gradient)
├── fitnes/                 ← FitZona (#84cc16, energetic gradient)
├── nekretnine/             ← ProNekretnine (#059669, full-width + search)
└── autoservis/             ← Auto Servis Speed (#dc2626, dark split)
```

Svaki folder sadrži:
- `index.html` — kompletan demo sajt za tu delatnost
- `theme.css`  — samo per-industry override (accent boja, hero, font)

## Deploy na GitHub Pages

1. Push na GitHub (`git push origin main`)
2. Otvori repo → **Settings** → **Pages**
3. Source: **Deploy from a branch** → branch: `main` / folder: `/ (root)`
4. Sačekaj 1–2 minuta, stranica je dostupna na:

```
https://mrpaki.github.io/rondo-demos/
```

Svaki demo je na:
```
https://mrpaki.github.io/rondo-demos/{slug}/
```

## Lokalni preview

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .

# Live Server (VS Code ekstenzija)
# Desni klik na index.html → "Open with Live Server"
```

## Prilagođavanje

1. Promeni sadržaj u `{slug}/index.html` (naziv firme, telefon, adresa, tekstovi)
2. Zameni `picsum.photos` slike pravim fotografijama (komentari u HTML-u označavaju mesta)
3. Zameni Google Maps placeholder iframe sa pravim embed kodom
4. Promeni accent boju u `{slug}/theme.css` ako treba

## Tehnički detalji

- Čist HTML5 / CSS3 / Vanilla JS — nema build koraka, nema dependencies
- Fontovi: [Inter](https://fonts.google.com/specimen/Inter) (sve), [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) (advokat, nekretnine)
- Slike: `https://picsum.photos` placeholder-i uz komentare za zamenu
- Responsive: mobile-first, testiran na 320px–1440px
- Accessibility: WCAG AA kontrast, keyboard navigacija, skip-to-content, aria atributi
- `prefers-reduced-motion`: animacije se automatski isključuju
- Fiksna "Demo traka" na dnu svake stranice sa linkom na rondo.rs/sr/usluge/novo

---

Kontakt: [rondo.rs](https://rondo.rs) · mr.paki@gmail.com
