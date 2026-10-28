# GitHub–Netlify check: weby OPF

**Dátum kontroly:** 28. 10. 2026 (Europe/Bratislava)  
**Účel:** stručný, opakovateľný prehľad obsahu dvoch webov a ich prepojenia GitHub → Netlify.  
**Rozsah:** GitHub repozitáre, produkčné stránky otvorené v prihlásenom prehliadači a prehľady projektov Netlify.

## Rýchly prehľad

| Web | Živá adresa | GitHub repozitár | Projekt Netlify | Stav pri kontrole |
| --- | --- | --- | --- | --- |
| Webové prezentácie OPF | [magnificent-creponne-b671ef.netlify.app](https://magnificent-creponne-b671ef.netlify.app/) | [roman-sperka/opf-web-presentations](https://github.com/roman-sperka/opf-web-presentations) | [magnificent-creponne-b671ef](https://app.netlify.com/projects/magnificent-creponne-b671ef/overview) | Produkčné nasadenie z GitHubu, vetva `main`; obsah stránky sa načítal. |
| Test webových aplikácií OPF | [webpres1.netlify.app](https://webpres1.netlify.app/) | [roman-sperka/opf-web-test](https://github.com/roman-sperka/opf-web-test) | [webpres1](https://app.netlify.com/projects/webpres1/overview) | Produkčné nasadenie z GitHubu, vetva `main`; obsah stránky sa načítal. |

## 1. Webové prezentácie OPF

- **Aktuálny obsah:** jednoduchá úvodná stránka s označením „OPF · Slezská univerzita v Opavě“, nadpisom „Webové prezentácie OPF“ a oznamom o prvej testovacej stránke publikovanej cez ChatGPT → GitHub → Netlify.
- **Zdroj stránky:** [index.html](https://github.com/roman-sperka/opf-web-presentations/blob/main/index.html). Ide o samostatný statický HTML súbor so štýlmi priamo v súbore.
- **Prepojenie:** [prehľad Netlify](https://app.netlify.com/projects/magnificent-creponne-b671ef/overview) uvádza „Deploys from GitHub“ a odkazuje na repozitár `roman-sperka/opf-web-presentations`.
- **Posledná overená obsahová verzia:** commit [`27f4e00`](https://github.com/roman-sperka/opf-web-presentations/commit/27f4e0090cb250adaeb12314b9e6e8372514cf8f), v Netlify uvedený ako aktuálne publikovaný 28. 10. 2026 o 20:20.

## 2. Test webových aplikácií OPF

- **Aktuálny obsah:** testovacia stránka s nadpisom „Automatická aktualizácia funguje!“, informáciou o publikovaní cez GitHub a Netlify a počítadlom s tlačidlami „Pridať +1“ a „Reset“.
- **Zdroj stránky:** [index.html](https://github.com/roman-sperka/opf-web-test/blob/main/index.html). Ide o samostatný HTML súbor so štýlmi a krátkym JavaScriptom pre počítadlo.
- **Prepojenie:** [prehľad Netlify](https://app.netlify.com/projects/webpres1/overview) uvádza „Deploys from GitHub“ a odkazuje na repozitár `roman-sperka/opf-web-test`.
- **Posledná overená obsahová verzia:** commit [`d5ed78c`](https://github.com/roman-sperka/opf-web-test/commit/d5ed78c137ae1b45dd8e1acd24ee85221d316da2), v Netlify uvedený ako aktuálne publikovaný 28. 10. 2026 o 20:34.

## Čo prepojenie potvrdzuje

1. Oba projekty Netlify ukazujú priamy odkaz na zodpovedajúci GitHub repozitár.
2. Produkčná aktivita Netlify pri oboch weboch uvádza nasadenie z vetvy `main` a commit, ktorý existuje v príslušnom repozitári.
3. Načítané živé stránky zodpovedajú obsahu súborov `index.html` v týchto repozitároch.

GitHub repozitáre sú verejné. Netlify označuje **projekt** ako súkromný a **produkčný web** ako verejný. Prístup anonymného návštevníka bez prihlásenia nebol osobitne overený.

## Ako zopakovať kontrolu

Napíš v chate napríklad: **„Aktualizuj GitHub–Netlify check podľa súboru `GITHUB_NETLIFY_CHECK.md` v repozitári `roman-sperka/opf-web-presentations`.“**

Pri opakovaní treba otvoriť oba živé weby, porovnať ich obsah s aktuálnymi `index.html`, skontrolovať prepojené repozitáre a posledné produkčné nasadenia v Netlify a potom aktualizovať dátum aj zistenia v tomto súbore. Tento dokument je snímka stavu v čase kontroly; sám sa neaktualizuje.

*Poznámka: uloženie alebo aktualizácia tohto Markdown súboru vytvorí nový commit v `opf-web-presentations` a môže spustiť ďalšie automatické nasadenie bez zmeny obsahu úvodnej stránky.*
