---
layout: default
title: Plot test
plotly: true
---

# Interactive plot test

Test page for the website pipeline: a Plotly figure exported from the notebook
(`exploration/leonard_semaine1.ipynb`) and embedded with a Jekyll include.
Hover to read values, drag to zoom, double-click to reset.

{% include plots/spy_2007_2010.html %}

<p class="plot-caption">SPY, the ETF that tracks the S&amp;P 500, from 2007 to 2010. Shaded: the 2008 crisis, from the market peak (9 Oct 2007) to the trough (9 Mar 2009).</p>

[Back to the story]({{ '/' | relative_url }})
