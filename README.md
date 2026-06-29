# Fretboard Note Trainer

Interaktív hangfelismerő gyakorló a fogólapon: válaszd ki a célhang összes
helyét basszusgitáron, gitáron vagy ukulelén. Jó találatnál zöld jelölés,
rossznál finom piros villanás, és meghallod a helyes hangot is.

Az egész alkalmazás egyetlen `index.html` fájl – nincs build lépés, nincs
függőség. Elég megnyitni egy böngészőben.

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

## Telepítés a kezdőképernyőre (iPad / telefon)

Mivel ez egy egyszerű weboldal, a böngésző **„Hozzáadás a kezdőképernyőhöz”**
funkciójával ikonként is elmentheted, és (majdnem) appként használhatod.
A hang csak egy érintés után indul – ezért kell egyszer a *„Hang
bekapcsolása”* gomb.
