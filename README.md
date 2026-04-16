# AHA Meble — strona internetowa

Strona stolarni AHA Meble (MNW Sp. z o.o.), Gdańsk.

## Stack

- Statyczny HTML (jeden plik `index.html` + `polityka-prywatnosci.html`)
- Deploy: Vercel (auto-deploy z main)
- Formularz: Formspree (wymagany ID — patrz niżej)
- Repo: github.com/PropsPlanet/aha-meble

## Workflow zmian

```bash
cd ~/Sites/aha-meble
# edytuj index.html
git add -A && git commit -m "opis zmiany"
git push origin main
# Vercel auto-deploy ~60s
```

## TODO przed go-live 24.04.2026

- [ ] **Formspree ID** — zarejestrować konto na formspree.io, podpiąć `kontakt@ahameble.pl` jako odbiorcę, wstawić ID w `index.html` (szukaj `FORMSPREE_ID_PLACEHOLDER`)
- [ ] **Domena ahameble.pl** — DNS z cyber_Folks → Vercel (A record `76.76.21.21` lub CNAME `cname.vercel-dns.com`)
- [ ] **SSL** — Vercel zrobi automatycznie po podpięciu domeny
- [ ] **Google Search Console** — dodać domenę, wysłać sitemap
- [ ] **Redirect 301** z stolarz-gdansk.com → ahameble.pl (w panelu cyber_Folks albo w DNS)
- [ ] **Test formularza** — wysłać testową wiadomość i sprawdzić czy dochodzi na kontakt@ahameble.pl
- [ ] **Emaile @ahameble.pl** — wybrać hosting (Zoho Mail free/lite albo Google Workspace)
- [ ] **Favicon .ico** — wygenerować z `favicon.svg` (np. realfavicongenerator.net) i wstawić

## Dane firmy (używane w stopce i schema.org)

- **MNW Sp. z o.o.**
- NIP: 957 106 71 37 · REGON: 221790146 · KRS: 0000441826
- Adres rejestrowy: ul. Batalionów Chłopskich 8, 83-000 Pruszcz Gdański
- Hala produkcyjna: ul. Narwicka 10, 80-557 Gdańsk
- Tel: +48 507 027 300
- Email: kontakt@ahameble.pl

## Kluczowe sekcje `index.html`

| Linie | Sekcja |
|---|---|
| 1-66 | `<head>` — meta, schema.org, fonts |
| 67-470 | `<style>` — CSS |
| 750-790 | Hero |
| 790-805 | Pasek materiałów (nowy) |
| 805-830 | Realizacje (galeria) |
| 830-880 | Proces (4 kroki) |
| 880-920 | B2B (dla architektów) |
| 920-950 | O nas + zespół |
| 950-1080 | FAQ |
| 1080-1140 | Kontakt + formularz |
| 1140-1160 | Footer |
| 1420-1470 | JS (form submit, modal, gallery) |

## Historia zmian

- **15-16.04.2026** — duża aktualizacja: hero copy, pasek materiałów, proces techniczny, O Nas przepisane, rozszerzone FAQ, formularz z RODO + Formspree, footer z pełnymi danymi, favicon SVG, polityka prywatności. Adres firmowy: Narwicka 10 (hala) + Batalionów Chłopskich (rejestrowy).
- **15.04.2026** — feedback ojca: Gdański → koniec, Oliwski → przedostatnia, usunięte zdjęcie chmielna_03 (duplikat)
- **18.03.2026** — pierwsza wersja na Vercel (aha-meble.vercel.app)
