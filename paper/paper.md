---
title: "lavaanExtra: Convenience Functions for Package *lavaan*"
tags:
  - R
  - psychology
  - statistics
  - visualization
  - structural equation modeling
authors:
  - name: Rémi Thériault
    orcid: 0000-0003-4315-6788
    affiliation: 1
affiliations:
  - name: "Department of Psychology, Université du Québec à Montréal, Québec, Canada"
    index: 1
date: "2023-03-04"
bibliography: paper.bib
output:
  rticles::joss_article
  # md_document:
  #   preserve_yaml: TRUE
  #   variant: "markdown_strict"
journal: JOSS
link-citations: yes
csl: apa.csl
---

# Summary

{lavaanExtra} is an R package that offers an alternative, vector-based syntax to 
package {lavaan}, as well as other convenience functions such as naming paths 
and defining indirect links automatically. It also offers convenience formatting 
optimized for a publication and script sharing workflow.

# Statement of need

There are many reasons to use R [@base2021] for analyzing and reporting data 
from research studies. R is more compatible with the ideals of open science 
[@quintana2020]. In contrast to commercial software: (a) it is free to use; (b) 
it makes it easy to share a fully comprehensive analysis script; (c) it is 
transparent as anyone can look at the formulas or algorithms used in a given 
package; (d) the community can quickly contribute new packages based on current 
needs; (e) it generates better-looking figures; and (f) it helps reduce 
copy-paste errors so common in psychology. The latter point is a substantial one 
because according to some estimates, up to 50% of articles in psychology have at 
least one statistical error [@nuijten2016prevalence].

However, R has a major downside for R novices: its steep learning curve due to 
its programmatic interface, in contrast to perhaps more user-friendly 
point-and-click software. Of course, this flexibility is also a strength, as the 
R community can, and increasingly does, mobilize to produce packages that make 
using R as easy as possible [e.g., the _easystats_ ecosystem @easystatsPackage]. 
The {rempsyc} package contributes to this momentum by providing convenience 
functions that remove as much friction as possible between your script and your 
manuscript (in particular, if you are using Microsoft Word).

There are mainly three things that go into a manuscript: text, tables, and 
figures. {rempsyc} does not generate publication-ready text summarizing analyses; 
for this, see the {report} package [@reportPackage]. Instead, {rempsyc} focuses 
on the production of publication-ready tables and figures. Below, I go over
a few quick examples of those.

# Examples Features

## Publication-Ready Tables

Formatting your table properly in R is already a time-consuming task, but 
fortunately several packages take care of the formatting within R [e.g., the 
{broom} or {report} packages, @broom2022; @reportPackage; and there are several
others]. Exporting these formatted tables to Microsoft Word remains a challenge 
however. Some packages do export to Word [e.g., @stanley2018reproducible], but 
their formatting is often rigid especially when using analyzes that are not
supported by default.

{rempsyc} solves this problem by allowing maximum flexibility: you manually 
create the data frame exactly the way you want, and then only use the magical 
function, `nice_table()`, on the resulting data frame. `nice_table()` works on
any data frame, even non-statistical ones like `mtcars`.




# Availability

The {lavaanExtra} package is licensed under the MIT License. It is available on 
CRAN, and can be installed using `install.packages("lavaanExtra")`. The full 
tutorial website can be accessed at: https://lavaanExtra.remi-theriault.com/. 
All code is open-source and hosted on GitHub, and bugs can be reported at 
https://github.com/rempsyc/lavaanExtra/issues/.

# Acknowledgements

I would like to thank Hugues Leduc, Jay Olson, Charles-Étienne Lavoie, and Björn 
Büdenbender for statistical or technical advice that helped inform some functions 
of this package and/or useful feedback on this manuscript. I would also like
to acknowledge funding from the Social Sciences and Humanities Research Council 
of Canada.

# References