# Zobrazení délky času

Vstupem je délka času v celých nezáporných sekundách.

## Režimy zobrazení

| Režim | Zápis jednotek | Výběr jednotek |
|-------|----------------|----------------|
| Plné | Celé názvy | Všechny nenulové jednotky |
| Zkratky | Třípísmenné zkratky | Všechny nenulové jednotky |
| Omezené | Celé názvy | Nejvýše dvě jednotky podle pravidla níže |
| Omezené zkratky | Třípísmenné zkratky | Nejvýše dvě jednotky podle pravidla níže |

## Jednotky

| Jednotka | Zkratka | Tvar pro 1 | Tvar pro 2 až 4 | Tvar pro 0 a 5 nebo více | Převod |
|----------|---------|------------|-----------------|--------------------------|--------|
| Rok      | `rok` | rok     | roky    | let    | 12 měsíců (360 dní) |
| Měsíc    | `mes` | měsíc   | měsíce  | měsíců | 30 dní |
| Den      | `den` | den     | dny     | dní    | 24 hodin |
| Hodina   | `hod` | hodina  | hodiny  | hodin  | 60 minut |
| Minuta   | `min` | minuta  | minuty  | minut  | 60 sekund |
| Sekunda  | `sek` | sekunda | sekundy | sekund | základní jednotka |

## Společná pravidla

- Rozlož čas od roků po sekundy. U každé jednotky použij zbytek po odečtení vyšších jednotek.
- Jednotky s nulovou hodnotou vynech. Je-li celá doba nulová, zobraz `0 sekund` nebo `0 sek` podle režimu.
- Celé názvy skloňuj podle hodnoty. Zkratky mají vždy stejný tvar a píšou se bez tečky.
- Mezi číslem a jednotkou i mezi jednotlivými částmi piš jednu mezeru. Čísla zapisuj bez úvodních nul.

## Výběr jednotek v omezených režimech

1. Zobraz nejvyšší nenulovou jednotku.
2. Je-li jednotka o jeden stupeň níže nenulová, zobraz ji jako druhou.
3. Jinak zkontroluj jednotku o dva stupně níže. Je-li nenulová, zobraz ji jako druhou.
4. Pokud se druhá jednotka takto nenajde, zobraz pouze nejvyšší jednotku. Zbývající hodnoty vynech bez zaokrouhlení.

Například po dnech zkontroluj hodiny a potom případně minuty. Pokud zbývají jen sekundy, zobraz pouze dny.

## Příklady

| Plné | Zkratky | Omezené | Omezené zkratky |
|------|---------|---------|-----------------|
| `0 sekund` | `0 sek` | `0 sekund` | `0 sek` |
| `39 sekund` | `39 sek` | `39 sekund` | `39 sek` |
| `1 minuta` | `1 min` | `1 minuta` | `1 min` |
| `1 hodina 2 minuty 59 sekund` | `1 hod 2 min 59 sek` | `1 hodina 2 minuty` | `1 hod 2 min` |
| `1 den 5 minut 9 sekund` | `1 den 5 min 9 sek` | `1 den 5 minut` | `1 den 5 min` |
| `1 den 9 sekund` | `1 den 9 sek` | `1 den` | `1 den` |
| `2 roky 3 měsíce 4 dny` | `2 rok 3 mes 4 den` | `2 roky 3 měsíce` | `2 rok 3 mes` |
