# Projekt 3 (Medium) - Antiyoy

> See on projekt 3 keerulisem variant. Lihtsama variandi leiad [siit](2026-03-20_projekt_3_easy.md). Üldinfo ja hindamine on [projekt 3 lehel](2026-03-20_projekt_3.md).

**Antiyoy** on strateegiamäng (iOS, Android). **Tinkr** on multiplayer kloon sellest. Kogu keerukas loogika on serveris juba olemas - sina pead serverist tuleva dataga mängu kuvama ja tegema funktsionaalsuse, et mängija saaks reaalselt mängida.

Kõik reeglid on serveris juba olemas. Sina pead tegema sellised käsud nagu `join`, `start`, `move`, `buy`, `end_turn`.

## Juhend

1. Kogu vajalik info on olemas [Tinkri dokumentatsioonis](https://tinkr.tech/sdb-ui/docs/antiyoy)
2. Loo endale ise andmebaas Antiyoy tüüpi
3. Fetchi data ja renderda kaart
4. Implementeeri actionid

## Ühendamine

Alguses on lihtsam arendada oma andmebaasiga, sest meie ühises serveris on taimerid, mis viskavad su välja või jätavad su käigu vahele. Oma serveris võid rahulikult tegutseda ja ka andmebaasi settingutest resettida. Kui mäng on valmis ühenda ta meie ühisesse serverisse: [https://tinkr.tech/sdb/poly/antiyoy](https://tinkr.tech/sdb/poly/antiyoy).
