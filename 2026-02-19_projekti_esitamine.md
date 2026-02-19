# Projekti esitamine

## Kuidas esitamine käib

1. Avalikustad oma lehe GitHub Pages abil (juhend allpool).
2. Kutsud õpetaja ja näitad toimivat lehte.
3. Õpetaja küsib küsimusi sinu koodi kohta — pead oskama seletada, mida iga osa teeb.

---

## GitHub Pages juhend

GitHub Pages võimaldab sul oma repo failidest teha päris veebilehe, mida saab brauseris avada.

### 1. Veendu, et su repos on `index.html`

GitHub Pages otsib automaatselt faili nimega `index.html`. Kui sinu fail on nimetatud kuidagi teisiti, nimeta see ümber:

```bash
mv minuleht.html index.html
```

Samuti veendu, et `style.css` ja `script.js` on samuti repos olemas ja pushitud.

### 2. Repo peab olema **Public**

GitHub Pages töötab tasuta ainult avalike repodega.

Kui su repo on praegu privaatne, mine GitHubis oma repo lehele:

1. **Settings** (ülemine menüü)
2. Keri alla kuni **Danger Zone**
3. **Change repository visibility** → vali **Public**
4. Kinnita muudatus

### 3. Pushid oma koodi GitHubi

Enne Pages sisselülitamist veendu, et viimane kood on GitHubis olemas:

```bash
git add .
git commit -m "valmis esitamiseks"
git push
```

### 4. Lülita GitHub Pages sisse

1. Mine oma repo lehele GitHubis.
2. Vajuta **Settings** (ülemine menüü).
3. Vasakust menüüst vali **Pages**.
4. **Source** alt vali **Deploy from a branch**.
5. **Branch** alt vali **main** ja kaust **/root**.
6. Vajuta **Save**.

### 5. Oota ~1 minut

GitHub ehitab su lehte. Oota umbes minut ja värskenda Settings → Pages lehte.

Seal tekib link kujul:

```
https://SINUNIMI.github.io/REPONIMI/
```

See link peaks seal samas settingute lehel ka end näitama. See ongi sinu lehe aadress. Ava see brauseris ja kontrolli, et kõik töötab.

### 6. Kui leht ei tööta

- Kontrolli, et fail on nimega täpselt `index.html` (mitte `Index.html` ega `index.HTML`).
- Kontrolli, et repo on **Public**.
- Kontrolli, et oled kõik muudatused commitinud ja pushinud.
- Oota paar minutit — vahel võtab aega.
- Vaata brauseris Developer Tools → Console, kas tuleb vigu.
