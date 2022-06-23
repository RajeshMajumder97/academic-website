---
date: "2021-08-23T00:00:00Z"
external_link: ""
image:
#  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
links:
- icon: book
  icon_pack: fas 
  name: Report
  url: https://drive.google.com/file/d/18LoUwhmqC4bRpdJa4Io0GeDjCxxV8vgW/view?usp=sharing  
- icon: github
  icon_pack: fab
  name: Code
  url: https://github.com/RajeshMajumder97/IPW-LASSO-SIMULATION/commit/ebc82a58c8739b3a8768add5371d3be5a07d9d21
#slides: example
summary: This is my M.Sc. final year project.
tags:
- Projects
title: Performance of LASSO when one or more covariate(s) is/are Missing Not at Random(MNAR)
url_code: ""
url_report: "https://drive.google.com/file/d/18LoUwhmqC4bRpdJa4Io0GeDjCxxV8vgW/view?usp=sharing"
url_slides: "https://drive.google.com/file/d/15GszdEXy5FgvLUlzbuuMiQaDFB38_gqE/view?usp=sharing"
url_video: ""
---

## About ##

This is my M.Sc. final year project.

I did this project under the supervision of my mentor [Dr. Sumanta Adhya, WBSU.](https://www.wbsu.ac.in/faculty/dr-sumanta-adhya/)

In this project, I have tried to see that, how LASSO will perform the variable selection tasks under the multicollinearity situation when the data is affected by the missing values where the missingness is not at random. I have investigated different LASSO solutions from simulated data sets and trying to find a method that will benefit us in this situation. In this project, I have proposed a new methodology, “Inverse Probability Weighted Logistic Lasso Estimation” which gives a better solution than complete case analysis under the MNAR mechanism.

here I have compared a total of five Lasso solution techniques, that is, "LASSO on Original Data set(when all known)", "LASSO on Complete Data set(removing all missing observations)", "IPW-LASSO on Complete Data set using known(actual) missing probabilities", "IPW-LASSO on Complete Data set using estimated(MLE) missing probabilities", and "IPW-LASSO on Complete Data set using estimated(Logistic LASSO) missing probabilities". And, have shown that "IPW-LASSO on Complete Data set using estimated(Logistic LASSO) missing probabilities" is the better solution than, simple complete case analysis; when the missing mechanism is MNAR.

***Keywords*** : *MNAR*, *Logistic Regression*, *LASSO*, *IPW*, *IPW-LASSO*.

{{% callout note %}}
Click the *Slide* button above to see the project presentation.
{{% /callout %}}

{{% callout note %}}
Click the *Report* button above to see the project document.
{{% /callout %}}

{{% callout note %}}
Click the *github* button above to see the R code.
{{% /callout %}}
