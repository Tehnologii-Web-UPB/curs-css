# CSS Course — Lab Materials

This repository hosts the starter kits we use during the “Tehnologii Web 2026” course. It contains the files we reference live, together with hands-on exercises that you can continue on your own afterwards.

> The complete solutions live on the `solutii` branch: <https://github.com/Tehnologii-Web-UPB/curs-css/tree/solutii> (compare with the starters: <https://github.com/Tehnologii-Web-UPB/curs-css/compare/main...solutii>). Try the exercises first, then use the branch for comparison.

## Repository layout

- `css-basics-start/` – Minimal HTML scaffold for the CSS introduction (linking stylesheets, selectors, inheritance, specificity).
- `css-padding_margin/` – Small demos that illustrate padding vs. margin; tweak values in the browser to see the effect immediately.
- `exercises/`
  - `box/` – Practice manipulating the CSS box model.
  - `table/` – Exercise focused on styling semantic tables.
- `layout_flex_0/` – Flexbox drill: container and item properties on five blocks.
- `layout_grid_0/` … `layout_grid_3/` – Progressive CSS Grid exercises: equal columns, fixed tracks, a 12-column shell, then named lines and template areas.
- `workshop/` – Guided workshop “Hoinărind prin lume”; HTML is complete while the CSS files are blank. Follow the instructions in `workshop/README.md`.

Most exercise folders have a `README.md` with the requirements. All assets are static. Open any `index.html` directly in your browser (double-click or use a live-server plugin) to preview the result.

### Checking out the solutions locally

```bash
git fetch origin solutii
git switch solutii
```

Return to the starter materials at any time with:

```bash
git switch main
```

## Feedback & contributions

If you spot typos or have improvement ideas, open an issue in the GitHub repository. Pull requests are welcome, but we keep `main` as the clean starter version while solution updates should target dedicated branches such as `solutii`.

