# AI-Assisted Mutation Testing

Diplomová práca: **Testovanie mutácií s podporou umelej inteligencie: Inteligentné procesy pre automatizované zabezpečenie kvality**

Cieľom projektu je preskúmať, ako môže umelá inteligencia zlepšiť praktické používanie mutation testingu. Mutation testing je silná technika na hodnotenie kvality testov, ale v praxi býva pomalá, výpočtovo náročná a výsledky môžu byť ťažšie interpretovateľné.

## Cieľ

Projekt sa zameriava na návrh a implementáciu prototypu, ktorý umožní cielenejšie a praktickejšie mutation testing workflowy pomocou AI agenta.

Jedna z ideí je nespúšťať mutation testing vždy na celom projekte, ale sústrediť sa iba na relevantné časti kódu, napríklad zmenené súbory alebo konkrétne riadky po refactoringu.

## Doterajšia práca

Doteraz som sa venoval hlavne týmto častiam:

- štúdium článkov o mutation testingu,
- analýza LLM-based mutation testing prístupov,
- porovnanie dostupných Python mutation testing frameworkov,
- výskum možností jednotlivých nástrojov, ich podporovaných mutátorov, reportov, test runnerov, konfigurácie a použiteľnosti,
- návrh targeted mutation testing workflowu,
- implementácia `line-filter` pre Cosmic Ray,
- úprava HTML reportu pre skrytie skipped mutácií,
- návrh RooCode skillu pre mutation testing workflow,
- implementácia Mutation MCP Servera pre spúšťanie Cosmic Ray na vybraných riadkoch.

## Možné ďalšie smerovanie

Ďalej sa projekt môže rozšíriť napríklad o:

- lepší výber relevantných testov,
- automatickú interpretáciu survived mutantov,
- detekciu ekvivalentných mutantov,
- odporúčanie nových testov pomocou LLM,
- výber vhodných mutation operátorov,
- porovnanie klasického a targeted mutation testingu,
- experimentálne vyhodnotenie na reálnych projektoch.

## Status

Projekt je zatiaľ vo fáze výskumu a experimentálneho prototypovania. Cieľom je overiť, ktoré časti mutation testing workflowu vie AI agent zmysluplne automatizovať a kde má takýto prístup najväčšiu praktickú hodnotu. Prípadne aké zmeny vo frameworkoch dokážu najvic developerom pomôcť.

