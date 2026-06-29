# Fretboard Note Trainer

Interaktív hangfelismerő gyakorló a fogólapon: válaszd ki a célhang összes
helyét basszusgitáron, gitáron vagy ukulelén. Jó találatnál zöld jelölés,
rossznál finom piros villanás, és meghallod a helyes hangot is.

Az alkalmazás statikus weboldal – nincs build lépés, nincs függőség. Elég
megnyitni egy böngészőben. **PWA**: telepíthető és internet nélkül is
működik (service worker + manifest).

## Élő verzió

GitHub Pages-en: **https://amedveczki.github.io/fretboard/**

(A link akkor él, ha a Pages be van kapcsolva – lásd lentebb.)

## GitHub Pages bekapcsolása

Két lehetőség van, mindkettő pár kattintás:

### A) Automatikus deploy (ajánlott)

A repó tartalmaz egy GitHub Actions workflow-t
(`.github/workflows/deploy.yml`), ami minden `main` ágra történő push után
automatikusan kiteszi az oldalt.

1. A repó **Settings → Pages** menüjében a *Source* alatt válaszd a
   **GitHub Actions** opciót.
2. Mergeld ezt az ágat a `main`-be (vagy pushold a `main`-re).
3. Az **Actions** fülön megnézheted a deploy futását; ha zöld, az oldal él a
   fenti címen.

### B) Deploy ágról (workflow nélkül)

1. **Settings → Pages → Source: Deploy from a branch**.
2. Ág: `main`, mappa: `/ (root)`, majd **Save**.
3. Pár perc múlva él az oldal.

## Helyi használat

Töltsd le az `index.html`-t és nyisd meg a böngésződben – ennyi.

## Telepítés appként (iPad / telefon / asztali gép)

Az oldal PWA, ezért a böngésző **„Hozzáadás a kezdőképernyőhöz”** / **„App
telepítése”** funkciójával külön ikonként, teljes képernyős appként
telepítheted. Telepítés után **offline is működik**. A hang csak egy
érintés után indul – ezért kell egyszer a *„Hang bekapcsolása”* gomb.

> Megjegyzés: a service worker és a PWA-telepítés csak `https://`-en (azaz a
> GitHub Pages címen) aktív, `file://`-ről megnyitva nem.

## Fájlok

- `index.html` – maga az alkalmazás
- `manifest.webmanifest` – PWA leíró (név, ikonok, színek)
- `sw.js` – service worker az offline gyorsítótárhoz
- `icons/`, `favicon.ico` – ikonok és favicon
- `.github/workflows/deploy.yml` – automatikus Pages deploy
