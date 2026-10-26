# Exercițiu — Tabel semantic

HTML-ul conține un tabel complet (`thead`, `tbody`, `tfoot`). Stilizează-l doar din CSS.

## Cerințe

1. Lasă 100px spațiu în jurul tabelului (`margin` pe `body`).
2. Tabelul și celulele au border doar sus și jos (fără laterale). Folosește `border-collapse: collapse` ca bordurile să nu se dubleze.
3. `td` și `th` au `padding: 10px`.
4. Celulele de antet (`th`) au fundal albastru și text alb.
5. Rândurile impare au un fundal deschis (`tr:nth-child(odd)`).
6. Totalul din `tfoot` e aliniat la stânga.

Bonus: de ce `tr:nth-child(odd)` nu schimbă culoarea rândului din `thead`? (indiciu: ce fundal are `th`?)
