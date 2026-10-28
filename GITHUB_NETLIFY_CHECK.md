# GitHub–Netlify check: weby OPF

**Posledná kontrola:** 28. 10. 2026, 20:57 (Europe/Bratislava)  
**Metóda:** GitHub cez prepojený účet; údaje o nasadení priamo z Netlify API; obsah produkčných URL cez priamu HTTP požiadavku. **Chrome sa nepoužil.**

## Výsledok

| Web | Produkčná adresa | GitHub zdroj | Výsledok kontroly |
| --- | --- | --- | --- |
| Webové prezentácie OPF | [magnificent-creponne-b671ef.netlify.app](https://magnificent-creponne-b671ef.netlify.app/) | [roman-sperka/opf-web-presentations](https://github.com/roman-sperka/opf-web-presentations) | Netlify `ready`, vetva `main`, produkčná stránka `HTTP 200`. |
| Test webových aplikácií OPF | [webpres1.netlify.app](https://webpres1.netlify.app/) | [roman-sperka/opf-web-test](https://github.com/roman-sperka/opf-web-test) | Netlify `ready`, vetva `main`, produkčná stránka `HTTP 200`. |

## 1. Webové prezentácie OPF

- **Aktuálny obsah:** úvodná stránka „Webové prezentácie OPF“ s označením „OPF · Slezská univerzita v Opavě“ a informáciou o publikovaní cez ChatGPT → GitHub → Netlify.
- **Zdroj:** [index.html](https://github.com/roman-sperka/opf-web-presentations/blob/main/index.html); samostatný HTML súbor so štýlmi.
- **Netlify projekt:** [magnificent-creponne-b671ef](https://app.netlify.com/projects/magnificent-creponne-b671ef/overview), ID `96763b33-5bf9-4298-b65f-c5603369e0fa`.
- **Priame overenie:** Netlify API vrátilo produkčné nasadenie `ready`, vetvu `main` a commit `9dd09a2460094a3e0ba1db0824a8c667f60bcb41`. Tento commit sa v čase kontroly zhodoval s vrcholom vetvy `main` na GitHube. Produkčná URL vrátila `HTTP 200`, názov „OPF | Webové prezentácie“ a očakávaný nadpis.
- **Čas nasadenia overeného pred uložením tejto správy:** 28. 10. 2026, 20:55 (Europe/Bratislava). Posledná zmena obsahu stránky je v commite [`27f4e00`](https://github.com/roman-sperka/opf-web-presentations/commit/27f4e0090cb250adaeb12314b9e6e8372514cf8f); novšie commity upravovali dokumentáciu.

## 2. Test webových aplikácií OPF

- **Aktuálny obsah:** stránka „Automatická aktualizácia funguje!“ s počítadlom a tlačidlami „Pridať +1“ a „Reset“.
- **Zdroj:** [index.html](https://github.com/roman-sperka/opf-web-test/blob/main/index.html); HTML, štýly a krátky JavaScript.
- **Netlify projekt:** [webpres1](https://app.netlify.com/projects/webpres1/overview), ID `d1e629a9-9f6d-4181-ad3c-fa07d3513401`.
- **Priame overenie:** Netlify API vrátilo produkčné nasadenie `ready`, vetvu `main` a commit [`d5ed78c`](https://github.com/roman-sperka/opf-web-test/commit/d5ed78c137ae1b45dd8e1acd24ee85221d316da2). Commit sa zhodoval s vrcholom vetvy `main` na GitHube. Produkčná URL vrátila `HTTP 200`, očakávaný nadpis a ovládacie prvky počítadla.
- **Čas publikovania:** 28. 10. 2026, 20:34 (Europe/Bratislava).

## Čo je overené a čo to znamená

- Oba aktuálne nasadené commity v Netlify sa zhodovali s príslušnou vetvou `main` na GitHube.
- Obe produkčné URL odpovedali priamo bez prihlásenia stavom `HTTP 200` a zobrazili očakávaný obsah.
- GitHub repozitáre sú verejné. Predchádzajúci prehľad Netlify označoval samotné projekty ako súkromné a produkčné weby ako verejné.
- Tento dokument je snímka stavu v uvedenom čase. Jeho uloženie vytvorí v `opf-web-presentations` ďalší dokumentačný commit, ktorý môže spustiť nové nasadenie bez zmeny `index.html`.

## Automatický postup pri vyvolaní

**Spúšťacia fráza:** „Aktualizuj GitHub–Netlify check“. Po jej prijatí vykonaj celý postup bez potreby ďalšieho zadania:

1. **GitHub:** v repozitároch `roman-sperka/opf-web-presentations` a `roman-sperka/opf-web-test` načítaj aktuálny commit vetvy `main` a obsah `index.html`.
2. **Netlify priamo:** načítaj údaje o projektoch cez Netlify API:
   - `GET https://api.netlify.com/api/v1/sites/96763b33-5bf9-4298-b65f-c5603369e0fa`
   - `GET https://api.netlify.com/api/v1/sites/d1e629a9-9f6d-4181-ad3c-fa07d3513401`
   Zisti stav `published_deploy`, vetvu, commit a čas publikovania. Podľa potreby načítaj `GET /api/v1/sites/{site_id}/deploys?per_page=5`, najmä po zápise tohto súboru.
3. **Živé weby:** priamou HTTP požiadavkou bez prehliadača načítaj `https://magnificent-creponne-b671ef.netlify.app/` a `https://webpres1.netlify.app/`. Over úspešný stav HTTP a základný obsah: pri prvom „Webové prezentácie OPF“, pri druhom „Automatická aktualizácia funguje!“ a ovládacie prvky počítadla.
4. **Porovnanie:** pri každom webe porovnaj nasadený commit Netlify s GitHub vetvou `main`. Rozlišuj stav `ready`, prebiehajúce nasadenie, chybu a rozdiel commitov. Zaznamenaj čas kontroly v `Europe/Bratislava`.
5. **Správa:** aktualizuj tento Markdown súbor faktami z novej kontroly. V odpovedi v chate vždy zobraz samostatne zrozumiteľný výsledok: stručné zhrnutie, tabuľku oboch webov s obsahom a stavom nasadenia, prípadné problémy a odkaz na tento súbor. Samotný odkaz nestačí.
6. **Overenie zápisu:** po uložení skontroluj, že je nový Markdown súbor na GitHube čitateľný. Zápis vytvorí ďalší commit v hlavnom repozitári; skontroluj cez Netlify API, či jeho automatické nasadenie dosiahlo stav `ready`. Výsledok tohto posledného nasadenia oznám v chate. Neprepisuj správu opakovane len kvôli zaznamenaniu jej vlastného commitu.

**Nepoužívaj používateľov Chrome ani jeho prihlásenú reláciu.** Ak priame Netlify overenie zlyhá, uveď presne, ktorá časť zostala neoverená. Starší stav nikdy neoznačuj za aktuálny. Tento check sa spúšťa na vyžiadanie uvedenou frázou; nemá samostatný časový plán.
