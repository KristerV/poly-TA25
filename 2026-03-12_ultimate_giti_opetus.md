# Ultimate Giti opetus

Siin on konkreetsed lahendused olukordadele kuhu sa Gitiga satud.

---

## 1. Kuidas alustada uut projekti?

### Samm 1: Tee repo GitHubis
1. Mine `github.com` peale
2. Vajuta rohelist nuppu **"New"** (või mine `github.com/new`)
3. Pane repole nimi (nt `minu-projekt`)
4. Jäta "Public" valituks
5. **Pane linnuke "Add a README file" peale** - see teeb elu lihtsamaks
6. Vajuta **"Create repository"**

### Samm 2: Klooni arvutisse
1. Repo lehel vajuta rohelist nuppu **"Code"**
2. Kopeeri HTTPS link
3. Ava Git Bash (Windows) või terminal (Mac)
```
git clone https://github.com/sinu-nimi/minu-projekt.git
```

### Samm 3: Mine projekti kausta
```
cd minu-projekt
```

### Samm 4: Tee oma failid
Ava see kaust Sublimes (File > Open Folder) ja tee oma failid, nt `index.html`, `style.css`.

### Samm 5: Pushige GitHubi
```
git add .
git commit -m "first commit with index and styles"
git push
```

### Samm 6: Kontrolli
Mine tagasi `github.com` oma repo peale ja vaata kas failid on kohal.

---

## 2. Tegin muudatused koodis, kuidas GitHubi saan?

Sul on juba projekt olemas ja kloonitud. Sa tegid muudatusi failides ja tahad need GitHubi üles saada.

```
git add .
```
See lisab KÕIK muudetud ja uued failid staging alasse. Punkt tähendab "kõik siin kaustas".

```
git status
```
Vaata üle, et rohelised failid on need mida tahad commitida.

```
git commit -m "kirjelda mida tegid"
```
See salvestab su muudatused lokaalse ajaloo sisse. Sõnum peaks olema lühike aga arusaadav, nt "added navbar styling" või "fixed broken link".

```
git push
```
See saadab su commitid GitHubi serverisse.

**Kontrolli tulemust:**
1. Mine `github.com` peale
2. Ava oma repo
3. Vaata kas failid on uuenenud ja kas su commit on näha

**Kiire versioon kõik korraga:**
```
git add .
git commit -m "sinu sõnum"
git push
```

---

## 3. Kuidas VIMist välja saada

Kui sa tegid `git commit` ilma `-m` liputa, või midagi muud läks valesti, ja sa oled kinni kummalises editoris kus midagi ei tööta - sa oled VIMis.

### Lahkumine SALVESTAMISEGA (commit läheb läbi):
```
:wq
```
Trüki täpselt nii: koolon, w, q, ja vajuta Enter. See salvestab ja väljub.

### Lahkumine ILMA salvestamata (tühistan commiti):
```
:q!
```
Koolon, q, hüüumärk, Enter. See väljub ilma salvestamata.

### Aga ma trükkisin mingit jama ja miski ei tööta??
1. Vajuta `Esc` (võib-olla mitu korda)
2. Siis trüki `:q!` ja Enter

**Pro tip:** Ära satu enam VIMi - kasuta alati `-m` lippu:
```
git commit -m "sinu sõnum siin"
```

---

## 4. Mu Git Bash ei ole sisse logitud (Windows)

Sa proovid `git push` teha aga saad errorit credentials kohta, või küsitakse username/password aga miski ei tööta.

### Lahendus: Git Credential Manager

Git Credential Manager tuleb tavaliselt koos Git for Windowsiga. Kui see töötab, siis esimese pushi ajal avaneb browser aken kus saad GitHubi sisse logida.

**Kui seda ei juhtu, kontrolli kas see on olemas:**
```
git credential-manager --version
```

**Kui seda ei ole, installi Git for Windows uuesti:**
1. Mine `gitforwindows.org`
2. Lae alla ja installi
3. Installimise ajal **veendu et "Git Credential Manager" on valitud** (see on default, ära tiki seda maha)

**Pärast installimist:**
```
git push
```
Nüüd peaks avanema brauseri aken kus saad GitHubi oma kontoga sisse logida. Pärast seda mäletab arvuti su loginit ja sa ei pea enam uuesti sisse logima.

**Kui ikka ei tööta, proovi käsitsi seadistada:**
```
git credential-manager configure
```

**Viimane abinõu - mine üle SSH peale:**
Kui miski ei aita, küsi õpetajalt SSH key seadistamise kohta. See on teine viis kuidas GitHubiga ühendust saada mis ei kasuta parooli.
