# Návlek – Blažek Glass Beads

Jednoduchá stránka pro rychlé dohledání **návleku** podle čísla artiklu a velikosti.
Odpadá listování papírovými šanony se zakázkami při psaní lístečků pro navlékárny.

## Jak to funguje

- Zadáš artikl (číslo nebo název, např. `112-19-001`, `heishi`) a případně velikost v mm.
- Stránka ukáže návlek, např. **30 × 10** = 30 ks na šňůrce, 10 šňůrek ve svazku.
- Kde se faktury rozcházejí, jsou uvedené obě varianty s poznámkou.

## Soubory

| Soubor | Co obsahuje |
|---|---|
| `index.html` | Celá stránka v jednom souboru – vzhled, logika i data (blok `page-data`). |

## Data

Data jsou uložená přímo v `index.html` jako JSON (blok `<script id="page-data">`).
Každý záznam má:

- `a` – artikl
- `s` – velikost (např. `6 mm`, `3x6 mm`)
- `t` – návlek (např. `30x10`)
- `n` – poznámka / zdroj (nepovinné)

Pravidla: artikl + velikost = vždy jeden návlek. Artikly zadané jen názvem se ukládají malými písmeny bez mezer.

## Spuštění

Stačí otevřít `index.html` v prohlížeči. Záznamy přidané přes stránku se mimo Claude ukládají jen v daném prohlížeči – trvalá změna = úprava dat v `index.html`.

Vytvořeno s pomocí Claude jako první krok k sadě interních nástrojů Blažek Glass Beads.
