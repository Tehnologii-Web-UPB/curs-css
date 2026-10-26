# Variabile CSS (custom properties)

Pagina este deja stilizată, dar aceleași valori (albastrul `#2563eb`, `1rem`, `8px`…) sunt copiate în zeci de locuri. Scopul exercițiului: refactorizează `css/styles.css` cu variabile CSS, fără să modifici HTML-ul, astfel încât pagina să arate **la fel** la final.

Documentație: [Using CSS custom properties (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascading_variables/Using_custom_properties)

## Pașii

1. **Declarare în `:root`.** Creează variabile după _rol_, nu după culoare: `--color-primary`, `--color-primary-hover`, `--color-text`, `--color-text-muted`, `--color-background`, `--color-surface`, `--color-border`, apoi `--space-xs`/`--space-sm`/`--space-md`/`--space-lg` și `--radius-sm`/`--radius-md`.
   De ce nu `--blue`? Pentru că în tema întunecată (pasul 6) „primary” poate să nu mai fie albastru.
2. **Folosire cu `var()`.** Înlocuiește fiecare valoare repetată cu `var(--nume)`. Încearcă și un fallback: `var(--color-accent, var(--color-primary))`.
3. **Scoping.** Fă ca `.callout` să folosească `--callout-accent`. Apoi `.callout--warning` trebuie să conțină **o singură** declarație: noua valoare pentru `--callout-accent`.
4. **Moștenire.** La fel pentru `.card--featured`: redefinește `--card-border` (și eventual `--card-border-width`) în loc să suprascrii proprietățile.
5. **Media query.** La `min-width: 700px` schimbă doar valorile `--space-*`. Observă că _toate_ componentele se adaptează.
6. **Temă întunecată.** În `@media (prefers-color-scheme: dark)` redefinește doar variabilele de culoare. Testează din DevTools → Rendering → _Emulate CSS prefers-color-scheme_.
7. **`calc()`.** Folosește o variabilă într-un calcul, de ex. `padding: calc(var(--space-md) * 1.5)`.

## Capcane de reținut

- Numele sunt _case-sensitive_: `--Color` și `--color` sunt variabile diferite.
- Variabilele **nu** pot fi folosite în condiția unui media query: `@media (min-width: var(--bp))` nu funcționează.
- O valoare greșită (de ex. `--space-md: red` folosită la `padding`) nu e o eroare de sintaxă: proprietatea devine „invalid at computed-value time” și primește valoarea moștenită sau inițială.
- O variabilă nu poate conține jumătate de nume de proprietate sau de selector; ea înlocuiește doar _valori_.
