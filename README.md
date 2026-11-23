# Crashes by sector: data story website

Data story of the ADA 2026 project, group 23.
Code and notebook: <https://github.com/epfl-ada/ada2026-ada-2026-project-group-23>

Live site: <https://leonard-amsler.github.io/ada-crises-sectors/>

The site is a plain Jekyll site built by GitHub Pages from the `main` branch.
Every push to `main` updates the site within a minute or two.

## Files

| Path | What it is |
|---|---|
| `_config.yml` | Site title, description, URL |
| `index.md` | The data story (one long page) |
| `_layouts/default.html` | The HTML around every page |
| `assets/css/style.css` | The style |
| `_includes/plots/` | Interactive Plotly charts exported from the notebook |
| `plot-test.md` | Test page with one interactive chart |

## How to add an interactive chart

1. Clone this repo next to the project repo (`ADA/project-repo` and `ADA/ada-crises-sectors`).
2. In the notebook, build a Plotly figure `fig` and run `from src.utils.web import save_plot_for_site` then `save_plot_for_site(fig, "my_chart")`. This writes `_includes/plots/my_chart.html` here.
3. In the page (e.g. `index.md`), put `{% include plots/my_chart.html %}` on its own line, where the chart should appear. The page needs `plotly: true` in its front matter.
4. Optional caption under it: `<p class="plot-caption">...</p>`.
5. Commit both the page and `_includes/plots/my_chart.html`, push to `main`, and check the live site after a minute. Never edit the exported file by hand: re-run the notebook instead.

If you upgrade Plotly in Python, update `plotly_js_version` in `_config.yml` (the version is written at the top of each exported file).
