---
date: "2022-03-16T00:00:00Z"
external_link: ""
image:
#  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
  
#slides: example
summary: How to calculate sample size.
tags:
- Blogs
title: Sample Size Calculation in R.

output:
  blogdown::html_page:
    toc: true
  
---

## The Why of Sample Size Calculations :

- In designing an experiment, a key question is : **How many individuals/subjects do I need for my experiment ?**

- Too small of a sample size can under detect the effect of interest in our experiment.

- Too large of a sample size may lead to unnecessary wasting of resources and individuals.

- We want our sample size to be *'just right'*.

- *The answer:* **Sample Size Calculation**.

- *Goal:* **We strive to have enough samples to resonably detect if it really is there without wasting limited resources on too many samples.**


## Key features of Sample Size Calculation :

- **Effect Size:** magnitude of the effect under the `\(H_1\)` (*alternative*). - the larger the effect size, the easier it is to an effect and require fewer samples.

- **Power:** Probability of correctly rejecting the `\(H_0\)`(*null*) if it is flse. i.e., ($1-\beta$), where `\(\beta\)`= Type-II Error.

- **Significance level($\alpha$):** Probability of falsely rejecting the null hypothesis even through it is true.  i.e., Type-I error.


## Effect Size :

- While Power and Significance level are usually set irrespective of the data, the effect size is a property of the sample data.

- It is essentially a function of the difference between the means of the null and alternative hypotheses over the variation (standard deviation) in the data.$$Effect\:Size \approx \frac{{|{\mu}_{H_1}-{\mu}_{H_0}}|}{\sigma}$$

- Note that, this sample size can also be calculated from the Confidence interval. But here we are ignoring that technique.


## Mathematical Formulas for calculating sample Sazes :

### (A) For Estimation :

![For Estimation](Sample Size estimation formula for Esimation point of view.PNG)

### (B) For testing :

![For Proportion](Sample Size estimation formula for testing Proportion.PNG)


![For Mean](Sample Size estimation formula for testing Mean.PNG)


![For Epidemiology Study Design](Sample Size estimation formula for Epidemiology.PNG)


![For Epidemiology Study Design](Sample Size estimation formula for Epidemiology_2.PNG)

## Sample Size Calculation in R :

-------------------------------------------------------------------------------
Table of R packages & functions for calculating Sample Size for different tests
-------------------------------------------------------------------------------

Name of test                                Package         Function
--------------------------                 ---------      ------------
One Mean T-test                               pwr         pwr.t.test()
Two Means T-test                              pwr         pwr.t.test()
Two Means T-test (unequal Sample)             pwr         pwr.t2n.test()
Paired T-test                                 pwr         pwr.t.test()
One-way ANOVA                                 pwr         pwr.anova.test()
Single Proportion Test                        pwr         pwr.p.test()
Two Proportions Test                          pwr         pwr.2p.test()
Two Proportion Test (unequal Sample)          pwr         pwr.2p2n.test()
Chi-Squared Test                              pwr         pwr.chisq.test()
Simple Linear Regression                      pwr         pwr.f2.test()
Multiple Linear Regression                    pwr         pwr.f2.test()
Correlation                                   pwr         pwr.r.test()
One Mean Wilcoxon Test                        pwr         pwr.t.test()+15%
Mann-Whitney Test                             pwr         pwr.t.test()+15%
Paired Wilcoxon Test                          pwr         pwr.t.test()+15%
Kruskal Wallace Test                          pwr         pwr.anova.test()+15%
Repeated Measures ANOVA                     WebPower      wp.rmanova()
Multi-way ANOVA (1 Category of interest)    WebPower      wp.kanova()
Multi-way ANOVA (>1 Category of interest)   WebPower      wp.kanova()
Non-Parametric Regression (Logistic)        WebPower      wp.logistic()
Non-Parametric Regression (Poisson)         WebPower      wp.poisson
Multilevel modeling: CRT                    WebPower      wp.crt2arm/wp.crt3arm
Multilevel modeling: MRT                    WebPower      wp.mrt2arm/wp.mrt3arm


## One Mean T-test :

- **Description:** This tests if a sample mean is any different from a set value for a normally distributed variable.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
1              0           0                0                      Yes         No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `\(Effect\:Size(D)= \frac{{|{\mu}_{H_1}-{\mu}_{H_0}}|}{\sigma}\)`

- **Example:(1)** **Is the average body temperature of college students any different from 98.6°F?**

- **Solution:** 
    - Here, `\(H_0\:: Avg\:Body\:temp.=98.6°F\)` and `\(H_0\:: Avg\:Body\:temp.\neq 98.6°F\)`
    
    - We will guess that the **effect sizes will be medium.**
    
    - For t-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.t.test(d = , sig.level = , power = , type = c("two.sample", "**one.sample**", "paired"))*
      
      - d= effect size
      - sig.level= significant level
      - power= power of test
      - type= type of test
      
    - **Answer of the problem:**
      
      ```r
          library(pwr)
          Pwer_t=pwr.t.test(d=0.5, sig.level=0.05, power=0.80, type="one.sample",alternative="two.sided")
          Pwer_t
      ```
      
      ```
      ## 
      ##      One-sample t test power calculation 
      ## 
      ##               n = 33.36713
      ##               d = 0.5
      ##       sig.level = 0.05
      ##           power = 0.8
      ##     alternative = two.sided
      ```
      
      ```r
          print(paste0("Sample Size by rounding off is:",round(Pwer_t$n,0)))
      ```
      
      ```
      ## [1] "Sample Size by rounding off is:33"
      ```
- **Example:(2)** **Calculate the sample size for the following scenarios (with `\(\alpha=0.05\)`, and power=0.80):**

  - **(i)** You are interested in determining if the average income of college freshman is less than Rs.20,000. You collect trial data and find that the mean income was Rs.14,500 (SD=6000).
  
  - **(ii)** You are interested in determining if the average sleep time change in a year for college freshman is different from zero. You collect the following data of sleep change (in hours).
  
      Variable                                   Values
    ------------   ---------------------------------------------------------
    Sleep Change    -0.55, 0.16, 2.6, 0.65, -0.23, 0.21, -4.3, 2, -1.7, 1.9

  - **(iii)** You are interested in determining if the average weight change in a year for college freshman is greater than zero.


- **Solution:** 
  
  - (i) You are interested in determining if the average income of college freshman is less than Rs.20,000. You collect trial data and find that the mean income was Rs.14,500 (SD=6000).
      
    - Effect size = `\((Mean_{H_1}-Mean_{H_0})/SD= (14,500-20,000)/6000 = -0.917\)`
    
    - One-tailed test  
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.t.test(d=-0.917, sig.level=0.05, power=0.80, type="one.sample", alternative="less")$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :9"
    ```
    
  - (ii) Effect size =$(Mean_{H_1}-Mean_{H_0})/SD =(-0.446-0)/1.96 = -0.228$
      
      - Two-tailed test
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.t.test(d=-0.228, sig.level=0.05, power=0.80, type="one.sample", alternative="two.sided")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 153"
      ```
  - (iii) *Try it by yourself.*


## Two Means T-test :

- **Description:** this tests if a mean from one group is different from the mean of another group for a normally distributed variable. AKA, testing to see if the difference in means is different from zero.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
1              1           2                1                      Yes         No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `\(Effect\:Size(D)= \frac{{|Mean_{H_1}-Mean_{H_0}}|}{SD_{pooled}}\)`

- **Example:(1)** **: Is the average body temperature higher in women than in men?**

- **Solution:** 
    - Here, `\(H_0\:: Avg\:difference\:Body\:temp.\:between\:men\:and\: women=0°F\)` and `\(H_1\:: Avg\:difference\:Body\:temp.\:between\:men\:and\: women>0°F\)`
    
    - We will guess that the **effect sizes will be medium.**
    
    - For t-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - Selected greater, because we only cared to test if women’s temp was higher, not lower (group 1 is women, group 2 is men)
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.t.test(d = , sig.level = , power = , type = c("**two.sample**", "one.sample", "paired"))*
      
      - d= effect size
      - sig.level= significant level
      - power= power of test
      - type= type of test
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round(pwr.t.test(d=0.5, sig.level=0.05, power=0.80,type="two.sample", alternative="greater")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :50"
      ```

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if the average daily caloric intake different between men and women. You collected trial data and found the average caloric intake for males to be 2350.2 (SD=258), while females had intake of 1872.4 (SD=420).
  
  - **(ii)** You are interested in determining if the average protein level in blood different between men and women. You collected the following trial data on protein level (grams/deciliter).
              
        Protein                         levels  
    --------------   ---------------------------------------
    Male Protein     1.8, 5.8, 7.1, 4.6, 5.5, 2.4, 8.3, 1.2
    Female Protein   9.5, 2.6, 3.7, 4.7, 6.4, 8.4, 3.1, 1.4

  - **(iii)** You are interested in determining if the average glucose level in blood is lower in men than women.
  

- **Solution:** 
  
  - (i) You are interested in determining if the average income of college freshman is less than Rs.20,000. You collect trial data and find that the mean income was Rs.14,500 (SD=6000).
      
    - Effect size = `\((Mean_{H1}-Mean_{H0})/ SD_{pooled} =(2350.2-1872.4)/ \sqrt{(2582+ 4202)/2} =477.8/348.54 = 1.37\)`
    
    - two-tailed test  
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.t.test(d=1.37, sig.level=0.05, power=0.80, type="two.sample",alternative="two.sided")$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :9"
    ```
    
  - (ii) Effect size =$(Mean_{H_1}-Mean_{H_0})/ SD_{pooled} =(4.59-4.98)/ \sqrt{(2.58^2+ 2.88^2)/2} = -0.14$
      
      - Two-tailed test
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.t.test(d=-0.14, sig.level=0.05, power=0.80, type="two.sample", alternative="two.sided")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 802"
      ```
  - (iii) *Try it by yourself.*


## Paired T-test :

- **Description:** : This tests if a mean from one group is different from the mean of another group, where the groups are dependent (not independent) for a normally distributed variable. Pairing can be leaves on same branch, siblings, the same individual before and after a trial, etc.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
1              1           2                1                      Yes         Yes      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `\(Effect\:Size(D)= \frac{{|Mean_{H_1}-Mean_{H_0}}|}{SD_{pooled}}\)`


- **Example:(1)** **Is heart rate higher in patients after a run compared to before a run?**

- **Solution:** 
    - Here, `\(H_0\::bpm(after) – bpm(before) \leq 0\)` and `\(H_1\:: bpm(after) – bpm(before)>0\)`
    
    - We will guess that the **effect sizes will be large.**
    
    - For t-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - Selected One-tailed, because we only cared if bpm was higher after a run.
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.t.test(d = , sig.level = , power = , type = c("two.sample", "one.sample", "**paired**"))*
      
      - d= effect size
      - sig.level= significant level
      - power= power of test
      - type= type of test
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round(pwr.t.test(d=0.8, sig.level=0.05, power=0.80, type="paired", alternative="greater")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :11"
      ```

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if metabolic rate in patients after surgery is different from before surgery. You collected trial data and found a mean difference of 0.73 (SD=2.9).
  
  - **(ii)** You are interested in determining if heart rate is higher in patients after a doctor’s visit compared to before a visit. You collected the following trial data and found mean heart rate before and after a visit.
              
      Heart rate                      levels  
    --------------   -----------------------------------------------------
    BPM before       126, 88, 53.1, 98.5, 88.3, 82.5, 105, 41.9
    BPM after        138.6, 110.1, 58.44, 110.2, 89.61, 98.6, 115.3, 64.3


- **Solution:** 
  
  - (i) You are interested in determining if metabolic rate in patients after surgery is different from before surgery. You collected trial data and found a mean difference of 0.73 (SD=2.9).
      
    - Effect size = `\((Mean_{H_1}-Mean_{H_0})/SD =(0.73)/ 2.9 = 0.25\)`
    
    - Two-tailed test  
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.t.test(d=0.25, sig.level=0.05, power=0.80, type="paired", alternative="two.sided")$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :128"
    ```
    
  - (ii) Effect size = `\((Mean_{H_1}-Mean_{H_0})/ SD_{pooled} =(98.1-85.4)/ \sqrt{(26.82+ 27.22)/2} =12.7/27 = 0.47\)`
      
      - One-tailed test
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.t.test(d=0.47, sig.level=0.05, power=0.80, type="paired", alternative="greater")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 29"
      ```


## One-Way ANOVA :

- **Description:** : This tests if at least one mean is different among groups, where the groups are larger than two, for a normally distributed variable. ANOVA is the extension of the Two Means T-test for more than two groups.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
1              1           > 2              1                      Yes        No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `$$Effect\:Size(f)=\sqrt{\frac{\eta^2}{1-\eta^2}}$$` Where, `$$\eta = \frac{SS_T}{TSS}=\frac{Treatment\:Sum\:Squares}{Total\:Sum\:Squares}$$` 

- **Example:(1)** **Is there a difference in new car interest rates across 6 different cities?**

- **Solution:** 
    - Here, `\(H_0\::0\)` and `\(H_1\:: \neq 0\)`
    
    - There are a total of 6 groups (cities).
    
    - We will guess that the **effect sizes will be small.**
    
    - For t-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - Groups assumed to be the same size.
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.anova.test(k =, f = , sig.level = , power = )*
      
      - k= number of groups
      - f= effect size
      - sig.level= significant level
      - power= power of test
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round(pwr.anova.test(k =6 , f =0.1 , sig.level=0.05 , power =0.80 )$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :215"
      ```

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining there is a difference in weight lost between 4 different surgery options. You collect the following trial data of weight lost in pounds.

      Surgery           Weight Measures  
    --------------   -------------------------
          A           6.3, 2.8, 7.8, 7.9, 4.9
          B           9.9, 4.1, 3.9, 6.3, 6.9
          C           5.1, 2.9, 3.6, 5.7, 4.5
          D           1.0, 2.8, 4.8, 3.9, 1.6

  
  
  - **(ii)** You are interested in determining if there is a difference in white blood cell counts between 5 different medication regimes.

- **Solution:** 
  
  - (i) Here, 
    
    - `\(\eta = SS_T/TSS=31.47/(31.47+62.87) = 0.33\)`
    Note that, you can calculate `\(SS_T\)` & `\(TSS\)` by performing ANOVA on the dataset using *aov()* function.
    
    - Effect size$(f)$ = `\(\sqrt{\eta^2/(1-\eta^2)}=\sqrt{0.33/(1- 0.33)} = 0.7\)`
    
    - No. of groups= 4
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.anova.test(k =4, f =0.7, sig.level=0.05, power =0.80 )$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :7"
    ```
    
  - (ii) You are interested in determining if there is a difference in white blood cell counts between 5 different medication regimes.
      
      - Guessed a medium effect size (0.25) 
      
      - No. of groups= 5
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.anova.test(k =5, f =0.25, sig.level=0.05, power =0.80 )$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 39"
      ```

## Single Proportion Test :

- **Description:** : This tests when you only have a single proportion and you want to know if the proportions of certain values differ from some constant proportion. 


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
0              1           2                 1                      N/A        No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `$$Effect\:Size(h)=2*(arcsin(\sqrt{p_{H_1}}))-2*(arcsin(\sqrt{p_{H_0}})))$$` 

- **Example:(1)** **Is there a significance difference in cancer prevalence of middle-aged women who have a sister with breast cancer (5%) compared to the general population prevalence (2%)?**

- **Solution:** 
    - Here, `\(H_0\::0\)` and `\(H_1\:: \neq 0\)`
    
    - You don’t have background info, so you guess that there is a small effect size.
    
    - For h-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - Selected Two-sided, because we don’t care about directionality.
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.p.test(h = , sig.level =, power =, alternative="two.sided", "less", or "greater" )*
      
      - h= effect size
      - sig.level= significant level
      - power= power of test
      - alternative= type of tail
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round( pwr.p.test(h=0.2, sig.level=0.05, power=0.80, alternative="two.sided")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :196"
      ```

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if the male incidence rate proportion of cancer in North Dakota is higher than the US average (prop=0.00490). You find trial data cancer prevalence of 0.00495.
  
  - **(ii)** You are interested in determining if the female incidence rate proportion of cancer in North Dakota is lower than the US average (prop=0.00420).


- **Solution:** 
  
  - (i) Here,
      
    - Effect size = `\(2*arcsin(\sqrt{0.00495})-2*arcsin(\sqrt{0.00490})=0.0007\)`. Note that, in R arcsin can be calculated by the function *asin()*. Difference of proportion power calculation for binomial distribution (arcsine transformation) 
    
    - One-sided test  
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.p.test(h=0.0007, sig.level=0.05, power=0.80, alternative="greater")$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :12617464"
    ```
    
  - (ii) You are interested in determining if the female incidence rate proportion of cancer in North Dakota is lower than the US average (prop=0.00420).
  
    - Guess a very low effect size (0.001)
      
      - One-tailed test
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.p.test(h=-0.001, sig.level=0.05, power=0.80, alternative="less")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 6182557"
      ```

## Two Proportions Test :

- **Description:** : this tests when you only have two groups and you want to know if the proportions of each group are different from one another.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
0              2           2                 2                      N/A        No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `$$Effect\:Size(h)=2*(arcsin(\sqrt{p_{H_1}}))-2*(arcsin(\sqrt{p_{H_0}})))$$` 

- **Example:(1)** **Is the expected proportion of students passing a stats course taught by psychology teachers different from the observed proportion of students passing the same stats class taught by mathematics teachers?**

- **Solution:** 
    - Here, `\(H_0\::0\)` and `\(H_1\:: \neq 0\)`
    
    - You don’t have background info, so you guess that there is a small effect size.
    
    - For h-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - Selected Two-sided, because we don’t care about directionality.
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.2p.test(h = , sig.level =, power =, alternative="two.sided", "less", or "greater" )*
      
      - h= effect size
      - sig.level= significant level
      - power= power of test
      - alternative= type of tail
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round( pwr.2p.test(h=0.2, sig.level=0.05, power=.80, alternative="two.sided")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :392"
      ```

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if the expected proportion (P1) of students passing a stats course taught by psychology teachers is different than the observed proportion (P2) of students passing the same stats class taught by biology teachers. You collected the following data of passed tests.

    Teaching Method                         Response  
    ---------------    -----------------------------------------------
      Psychology        Yes, Yes, Yes, No, No, Yes, Yes, Yes, Yes, No
       Biology          No, No, Yes, Yes, Yes, No, Yes, No, Yes, Yes
  
  
  - **(ii)** You are interested in determining of the expected proportion (P1) of female students who selected YES on a question was higher than the observed proportion (P2) of male students who selected YES. The observed proportion of males who selected yes was 0.75.


- **Solution:** 
  
  - (i) Here, 
    
    - `\(p_1=7/10=0.70, p_2=6/10=0.60\)`
    Note that, you can calculate `\(SS_T\)` & `\(TSS\)` by performing ANOVA on the dataset using *aov()* function.
    
    - Effect size= `\(h= 2*asin(\sqrt{0.60})-2*asin(\sqrt{0.70})=-0.21\)`
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.2p.test(h=-0.21, sig.level=0.05, power=0.80, alternative="two.sided")$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :356"
    ```
    
  - (ii) You are interested in determining if there is a difference in white blood cell counts between 5 different medication regimes.
      
      - Guess that the expected proportion `\((p_1)\)` =0.85 
      
      - Effect Size= `\(h= 2*asin(\sqrt{0.85})-2*asin(\sqrt{0.75})=0.25\)`
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.2p.test(h=0.25, sig.level=0.05, power=0.80, alternative="greater")$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 198"
      ```

## Chi-Squared Test :

- **Description:** : this tests when you only have two groups and you want to know if the proportions of each group are different from one another.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
`\(0\)`              `\(\geq 1\)`     `\(\geq 2\)`                1                N/A      No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `$$Effect\:Size(w)=\sqrt{\frac{{\chi}^2}{n\times df}}$$` where, `$${\chi}^2=\sum{\frac{(O_i-E_i)^2}{E_i}}$$` 

- **Example:(1)** **Does the observed proportions of phenotypes from a genetics experiment different from the expected 9:3:3:1? **

- **Solution:** 
    - Here, `\(H_0\::0\)` and `\(H_1\:: \neq 0\)`
    
    - You don’t have background info, so you guess that there is a small effect size.
    
    - For w-tests: **0.1=small**, **0.3=medium**, and **0.5=large** effect sizes.
    
    - Degrees of freedoms= (the number of proportions minus 1) = 4 (phenotypes) – 1 = 3
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.chisq.test(w =, df = , sig.level =, power = )*
      
      - w= effect size
      - df= degrees of freedom
      - sig.level= significant level
      - power= power of test
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round(pwr.chisq.test(w=0.3, df=3, sig.level=0.05, power=0.80)$N,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :121"
      ```

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if the ethnic ratios in a company differ by gender. You collect the following trial data from 200 employees.

    Gender    White   Black   Am.Indian    Asian  
    -------  ------  ------  -----------  -------
    Male      0.60    0.25       0.01       0.14
    Female    0.65    0.21       0.11       0.03
    
  
  
  - **(ii)** You are interested in determining if the proportions of student by year (Freshman, Sophomore, Junior, Senior) is any different from 1:1:1:1. You collect the following trial data.

    --------------   -----------------------------------------------------------------------
      Student        1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20
       Grade         Frs, Frs, Frs, Frs, Frs, Frs, Frs, Soph, Soph, Soph, Soph, Soph, Jun, Jun, Jun, Jun, Jun, Sen, Sen, Sen    

- **Solution:** 
  
  - (i) Note that,
  
    - If they were equal the expected ratios should be the same as the overall ethnic ratios (62.5, 23.0, 6.0, 8.5) 
    
    - Will just focus on males
    
    - `\(\chi^2= \sum{\frac{(O_i-E_i)^2}{E_i}} = (60-62.5)2/62.5 + (25-23)2/23 + (1-6)2/6 + (14-8.5)2/8.5 = 8\)`
    
    - Effect size= `\(w = \sqrt{\chi^2 /(n*df)}= \sqrt{8/(200*3)}=0.115\)`
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(pwr.chisq.test(w=0.115, df=3, sig.level=0.05, power=0.80)$N,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :824"
    ```
    
  - (ii) Note that here,
      
      - `\(\chi^2= \sum{\frac{(O_i-E_i)^2}{E_i}} =  (7-5)^2/5 + (5-5)^2/5 + (5-5)^2/5 + (3-5)^2/5 = 1.6\)` 
      
      - Effect Size= `\(w = \sqrt{\chi^2 /(n*df)}= \sqrt{1.6/(20*3)}=0.163\)`
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.chisq.test(w=0.163, df=3, sig.level=0.05, power=0.80)$N,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 410"
      ```


## Simple & Multiple Linear Regression :

- **Description:** :  this test determines if there is a significant relationship between two or more normally distributed numerical variables. The predictor variable is used to try to predict the response variable.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
2 or >2         0           NA                 NA                    Yes        No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `$$Effect\:Size(f2)=\sqrt{R^2}$$` Where, `$$R^2= Goodness\:of \:fit\:measure(i.e., Adjusted\:R^2)$$` 

- **Example:(1)** **Is there a relationship between height and weight in college males?**

- **Solution:** 
    - Here, `\(H_0\::0\)` and `\(H_1\:: \neq 0\)`
    
    - You don’t have background info, so you guess that there is a small effect size.
    
    - For `\(f2\)`-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - For simple regression (only one predictor variable) = numerator df=1 & for multiple regression it is just the number of predictor variables.
    
    - Output will be denominator degrees of freedom rather than sample size; will need to round up and add 2 for simple linear regression & add p+1; (where p= No. of predictor+1, because there is only one dependent outcome variable) for multiple linear regression  to get sample size.

    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.f2.test(u =, v= , f2=, sig.level =, power = )*
      
      - u= numerator degrees of freedom
      - v= denominator degrees of freedom
      - f2= effect size
      - sig.level= significant level
      - power= power of test
    
    - To calculate sample size: Sample Size(n)= **(denominator degrees of freedom(v) + Total No. of variables)**
    
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round( pwr.f2.test(u=1, f2=0.35, sig.level=0.05, power=0.80)$v,0)+2)) ##--2 has add because it is a simple linear regression
      ```
      
      ```
      ## [1] "The Sample Size is :25"
      ```

- **Example: (2)** **You are interested in determining if height (meters), weight (grams), and fertilizer added (grams) in plants can predict yield (grams of berries). You collect the following trial data. Here `\(\alpha=0.05\)`, & `\(Power=(1-\beta)=80%\)`**

    Variables             Values
    -------------  -------------------------------
     Yield         46.8, 48.7, 48.4, 53.7, 56.7
     Height        14.6, 19.6, 18.6, 25.5, 20.4
     Weight        95.3, 99.5, 94.1, 110, 103
     Fertilizer    2.1, 3.2, 4.3, 1.1, 4.3

- **Solution:** 
    - Here, at first we have to find the `\(Adjusted\:R^2\)` value by fitting the linear model.
    
    - Then, we will find the sample size.
    
    - **R Code :**
    
    
    ```r
    #--Data--#
    yield= c(46.8, 48.7, 48.4, 53.7, 56.7)
    height= c(14.6, 19.6, 18.6, 25.5, 20.4)
    weight= c(95.3, 99.5, 94.1, 110, 103)
    Fert= c(2.1, 3.2, 4.3, 1.1, 4.3)
    
    #-- Fitting Linear Model --#
    Model= lm(height~yield + weight + Fert)
    
    #-- Extracting Adjusted R^2 Value --#
    R_Sqared= summary(Model)$adj.r.squared
    
    #-- Calculating Effect (f2) --#
    f.2= sqrt(R_Sqared)
    
    #--  Calculating sample size --#
    ##--4 has added because it is a multiple linear Regression with 3 predictors and one dependent variable--##
    
    print(paste0("The Sample Size is :",round( pwr.f2.test(u=1, f2=f.2, sig.level=0.05, power=0.80)$v,0)+4))
    ```
    
    ```
    ## [1] "The Sample Size is :14"
    ```
    

## Correlation :

- **Description:** : This test determines if there is a difference between two numerical values. It is like simple regression, but is not identical.


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
2               0           NA               NA                     Yes        No      
------------------------------------------------------------------------------------


- **Effect size calculation:** Effect Size= r= Correlation Coefficient

- **Example:(1)** **Is there a correlation between hours studied and test score? **

- **Solution:** 
    - Here, `\(H_0\::r=0\)` and `\(H_1\:: r\neq 0\)`
    
    - You don’t have background info, so you guess that there is a small effect size.
    
    - For Correlation levels (r): **0.1=small**, **0.3=medium**, and **0.5=large** correlations.
    
    - Here approximate correlation power calculation is done by arctangh transformation 
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.r.test(r = , sig.level = , power = )*
      
      - r= correlation
      - sig.level= significant level
      - power= power of test
      
    - **Answer of the problem:**
      
      ```r
      print(paste0("The Sample Size is :",round(pwr.r.test(r=0.5, sig.level=0.05, power=0.80)$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is :28"
      ```
      
- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if there is a correlation between height and weight in men.

         Males                 Measures  
    ---------------    ------------------------
         Height        178, 166, 172, 186, 182
         Weight        165, 139, 257, 225, 196
  
  
  - **(ii)** You are interested in determining if, in lab mice, the correlation between longevity (in months) and average protein intake (grams).


- **Solution:** 
  
  - (i) Here, 
    
    - first, calculate the correlation value, and then calculate the sample size.
    
    - **R Code:**
    
    ```r
    #-- Data --#
    MH= c(178,166,172,186,182)
    MW= c(165,139,257,225,196)
    
    #-- correlation value --#
    
    r= cor(MH,MW)
    print(paste0("The Sample Size is :",round(pwr.r.test(r=0.37, sig.level=0.05, power=0.80)$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :54"
    ```
    
  - (ii)You are interested in determining if, in lab mice, the correlation between longevity (in months) and average protein intake (grams).
      
      - Guessed large (0.5) correlation
      
      - **R Code:**
      
      ```r
      print(paste("The Sample Size is :",round(pwr.r.test(r=0.5, sig.level=0.05, power=0.80)$n,0)))
      ```
      
      ```
      ## [1] "The Sample Size is : 28"
      ```

## Non-Parametric T-tests :

- **Description:** versions of the t-tests for non-parametric data.
  - *$\color{red}{\text{One Mean Wilcoxon:}}$* sample mean against set value
  - *$\color{red}{\text{Mann-Whitney:}}$* two sample means (unpaired)
  - *$\color{red}{\text{Paired Wilcoxon:}}$* two sample means (paired)


Name                                      Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
----------------------------------------- -------------- ----------- ---------------- ---------------------- ---------- ------
`\(\color{red}{\text{One Mean Wilcoxon:}}\)`   1              0           0                0                      No         NA    
`\(\color{red}{\text{Mann-Whitney:}}\)`        1              1           2                1                      No         No  
`\(\color{red}{\text{Paired Wilcoxon:}}\)`     1              1           2                1                      No         Yes
------------------------------------------------------------------------------------------------------------------------------


- **Effect size calculation:**  `\(\text{Effect Size}\;(\text{Cohen’s D:})= \frac{{|{\mu}_{H_1}-{\mu}_{H_0}}|}{\sigma};\frac{{|{\mu}_{H_1}-{\mu}_{H_0}}|}{\sigma_{pooled}};\frac{{\mu}_{\text{diff}}}{\sigma_{\text{diff}}}\)`

- **Example:(1)** **(for t-tests, 0.2=small, 0.5=medium, and 0.8 large effect sizes)**
  - (1) *$\color{red}{\text{One Mean Wilcoxon:}}$* **Is the average number of children in Grand Forks families different than 1?**

  - **Solution:** 
    - Here, `\(H_0\:: 1\;\text{child}\)` and `\(H_1\:: >1\;\text{child}\)`
    
    - You don’t have background info, so you guess that there is a **medium effect size.**
    
    - Select one-tailed (greater)
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.t.test(d = , sig.level = , power = , type = c("two.sample", "**one.sample**", "paired")) + 15%*
      
      - d= effect size
      - sig.level= significant level
      - power= power of test
      - type= type of test
      
    - **Answer of the problem:**
    
    ```r
    Pwer_t=pwr.t.test(d=0.5, sig.level=0.05, power=0.80, type="one.sample", alternative="greater")
    
    ##-- Nonparametric Correction : adding 15% --##
    print(paste0("Sample Size : ",round((Pwer_t$n*1.15),0)))
    ```
    
    ```
    ## [1] "Sample Size : 30"
    ```
  - (2) *$\color{red}{\text{Mann-Whitney:}}$* **Does the average number of snacks per day for individuals on a diet differ between young and old persons?**
  
  - **Solution:**
    - Here, `\(H_0\:: 0\;\text{difference in snack number, }\)` and `\(H_1\:: \neq 0\;\text{difference in snack number}\)`
    
    - You don’t have background info, so you guess that there is a **small effect size**
    
    - Select two-sided
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.t.test(d = , sig.level = , power = , type = c("**two.sample**", "one.sample", "paired")) + 15%*
      
      - d= effect size
      - sig.level= significant level
      - power= power of test
      - type= type of test
      
    - Note: [**"Parametric t-test + 15% Approach"** for calculating Sample Size for Non Parametric test](https://www.graphpad.com/guides/prism/7/statistics/stat_sample_size_for_nonparametric_.htm)
    
    - **Answer of the problem:**
    
    ```r
    Pwer_t=pwr.t.test(d=0.2, sig.level=0.05, power=0.80, type="two.sample", alternative="two.sided")
    
    ##-- Nonparametric Correction : adding 15% --##
    print(paste0("Sample Size : ",round((Pwer_t$n*1.15),0)))
    ```
    
    ```
    ## [1] "Sample Size : 452"
    ```
  - (3) *$\color{red}{\text{Paired Wilcoxon:}}$* **Is genome methylation patterns different between identical twins?**
  
  - **Solution:**
    - Here, `\(H_0\::\text{0% methylation}\)` and `\(H_1\:: \neq \text{0% methylation}\)`
    
    - You don’t have background info, so you guess that there is a **large effect size**
    
    - Select one-tailed (greater)
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.t.test(d = , sig.level = , power = , type = c("two.sample", "one.sample", **"paired"**)) + 15%*
      
      - d= effect size
      - sig.level= significant level
      - power= power of test
      - type= type of test
      
    - **Answer of the problem:**
    
    ```r
    Pwer_t= pwr.t.test(d=0.8, sig.level=0.05, power=0.80, type="paired", alternative="greater")
    
    ##-- Nonparametric Correction : adding 15% --##
    print(paste0("Sample Size : ",round((Pwer_t$n*1.15),0)))
    ```
    
    ```
    ## [1] "Sample Size : 13"
    ```
  
  
  
- **Example:(2)** **Calculate the sample size for the following scenarios (with `\(\alpha=0.05\)`, and power=0.80):**

  - **(i)** You are interested in determining if the average number of pets in Grand Forks families is greater than 1. You collect the following trial data for pet number.

      Variable                 Values
    ------------   ------------------------------
        Pets       1, 1, 1, 3, 2, 1, 0, 0, 0, 4

  
  - **(ii)** You are interested in determining if the number of meals per day for individuals on a diet is higher in younger people than older. You collected trial data on meals per day.

      Variable               Values
    -------------   -------------------------
     Young meals     1, 2, 2, 3, 3, 3, 3, 4
     Older meals     1, 1, 1, 2, 2, 2, 3, 3
    

  - **(iii)** You are interested in determining if genome methylation patterns are higher in the first fraternal twin born compared to the second. You collected the following trial data on methylation level difference (in percentage).

       Variable                            Values
    --------------   ----------------------------------------------
    Methy.Diff(%)     5.96, 5.63, 1.25, 1.17, 3.59, 1.64, 1.6, 1.4

- **Solution:** 
  
  - (i) You are interested in determining if the average income of college freshman is less than Rs.20,000. You collect trial data and find that the mean income was Rs.14,500 (SD=6000).
      
    - Effect size = `\((Mean_{H_1}-Mean_{H_0})/SD= (1.3-1.0)/1.34 =0.224\)`
    
    - One-tailed test  
    
    - **R Code:**
    
    ```r
    Pwer_t= pwr.t.test(d=0.224, sig.level=0.05, power=0.80, type="one.sample", alternative="greater")
    
    #-- Non-parametric Correction --# 
    print(paste0("The Sample Size is :",round(Pwer_t$n*1.15,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :143"
    ```
    
  - (ii)  *Try it by yourself.*
  
  - (iii) *Try it by yourself.*


## Kruskal Wallace Test :

- **Description:** : this tests if at least one mean is different among groups, where the groups are larger than two for a non-normally distributed variable. (AKA, non-parametric ANOVA). There really isn’t a good way of calculating sample size in R, but you can use a rule of thumb: 
  
  - Run Parametric Test
  - Add 15% to total sample size


Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
1               1           >2               1                      No         No      
------------------------------------------------------------------------------------


- **Effect size calculation:** Effect Size = Same as the effect size for the ANOVA.

- **Example:(1)** ** Is there a difference in draft rank across 3 different months? **

- **Solution:** 
    - Here, `\(H_0\::r=0\)` and `\(H_1\:: r\neq 0\)`
    
    - There will be a total of 3 groups (months)
    
    - You don’t have background info, so you guess that there is a **medium effect size.**
    
    - For `\(\text{f-test}\)` : **0.1=small**, **0.25=medium**, and **0.4=large** correlations.
    
    - No Tails in ANOVA
    
    - Groups assumed to be the same size.
    
    - **R Package:** *pwr* Package
    
    - **R function:** *pwr.anova.test(k =, f = , sig.level = , power = )*
      
      - k= number of groups
      - f= effect size
      - sig.level= significant level
      - power= power of test
      
    - **Answer of the problem:**
    
    ```r
      ##-- Balanced one-way analysis of variance power calculation --##
      Pwr_Anova=  pwr.anova.test(k =3 , f =0.25 , sig.level=0.05 , power =0.80 )
      
      #-- Non-parametric Correction --#
      print(paste0("The Sample Size is :",round((Pwr_Anova$n*1.15),0)))
    ```
    
    ```
    ## [1] "The Sample Size is :60"
    ```


- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining there is a difference in hours worked across 3 different groups(faculty, staff, and hourly workers). You collect the following trial data of weekly hours.

        Groups            Working Hours  
    --------------   -------------------------
       Faculty        42, 45, 46, 55, 42
        Staff         46, 45, 37, 42, 40
       Hourly         29, 42, 33, 50, 23

  
  
  - **(ii)** You are interested in determining there is a difference in assistant professor salaries across 25 different departments.

- **Solution:** 
  
  - (i) Here, 
    
    - `\(\eta^2 = SS_T/TSS=286.5/(286.5+625.2) = 0.314\)`
    Note that, you can calculate `\(SS_T\)` & `\(TSS\)` by performing ANOVA on the dataset using *aov()* function.
    
    - Effect size$(f)$ = `\(\sqrt{\eta^2/(1-\eta^2)}=\sqrt{0.314/(1- 0.314)} = 0.677\)`
    
    - No. of groups= 3
    
    - **R Code:**
    
    ```r
      ##-- Balanced one-way analysis of variance power calculation --##
      Pwr_Anova=  pwr.anova.test(k =3, f =0.677, sig.level=0.05, power =0.80)
      
      #-- Non-parametric Correction --#
      print(paste0("The Sample Size is :",round((Pwr_Anova$n*1.15),0)))
    ```
    
    ```
    ## [1] "The Sample Size is :9"
    ```
    
  - (ii) You are interested in determining there is a difference in assistant professor salaries across 25 different departments.

      - Guess small effect size (0.10)
      
      - No. of groups= 25
      
      - **R Code:**
      
      
      ```r
        #-- Balanced one-way analysis of variance power calculation --#
        Pwr_Anova= pwr.anova.test(k =25, f =0.10, sig.level=0.05, power =0.80)
      
        #-- Non-parametric Correction --#
        print(paste0("The Sample Size is :",round((Pwr_Anova$n*1.15),0)))
      ```
      
      ```
      ## [1] "The Sample Size is :104"
      ```


## Repeated Measures ANOVA :

- **Description:** : this tests if at least one mean is different among groups, where the groups are repeated measures (more than two) for a normally distributed variable. Repeated Measures ANOVA is the extension of the Paired T-test for more than two groups.



Numeric Var(s) Cat. Var(s) Cat. Var Group # Cat. Var # of interest Parametric Paired
-------------- ----------- ---------------- ---------------------- ---------- ------
1              1           > 2              1                       Yes        No      
------------------------------------------------------------------------------------


- **Effect size calculation:**  `$$Effect\:Size(f)=\frac{\sigma_m}{\sigma}$$` Where, `$$\sigma_m=\sqrt{\frac{\sum_{j=1}^K{(m_j-m)^2}}{k}}= Standard\:Deviation\:of\:group\:means$$` `$$m_j= j^{th}\:group\:mean\:,\:\:\forall\:j=1(1)K$$` `$$m=Overall\:mean$$` `$$K=number\:of\:groups$$` `$$\sigma=overall\:standard\:deviation$$`

- **Example:(1)** **Is there a difference in blood pressure at 1, 2, 3, and 4 months post-treatment?**

- **Solution:** 
    - Here, `\(H_0\::0\)` and `\(H_1\:: \neq 0\)`
    
    - **1 group**, **4 measurements**
    
    - We will guess that the **effect sizes will be small.**
    
    - For t-tests: **0.2=small**, **0.5=medium**, and **0.8=large** effect sizes.
    
    - For the nonsphericity correction coefficient, 1 means sphericity is met. There are methods to estimate this but will go with 1 for this example.
    
    - **R Package:** *WebPower* Package
    
    - **R function:** *wp.rmanova(ng = NULL, nm = NULL, f = NULL, nscor = 1, alpha = 0.05, power = NULL, type = 0) *
      
      - ng= number of groups
      - nm= number of measurements
      - f= effect size
      - nscor= nonsphericity correction coefficient
      - alpha= significant level of test
      - power= statistical power
      - type= (0,1,2) The value "0" is for between-effect; "1" is for within-effect; and "2" is for interaction effect.
      
      - **Note:** 
        - **Within-effects:** variability of a particular value for individuals in a sample
        - **Between-effects:** examines differences between individuals
      
    - **Answer of the problem:**
    
    ```r
    library(WebPower)
    print(paste0("The Sample Size is :",round(wp.rmanova(n=NULL, ng=1, nm=4, f=0.1, nscor=1, alpha=0.05, power=0.80, type=1)$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :1092"
    ```
    - Note:
    
     - [Power analysis for within-effect test](https://webpower.psychstat.org/wiki/manual/power_of_rmanova#power_curve)
     - [Sphericity and Repeated Measures ANOVA](https://stattrek.com/anova/repeated-measures/sphericity.aspx)

- **Example:(2)** **Calculate the sample size for the following scenarios (with α=0.05, and power=0.80):**

  - **(i)** You are interested in determining if there is a difference in blood serum levels at 6, 12, 18, and 24 months post-treatment. You collect the following trial data of blood serum in mg/dL.

        Months              Blood Serum  
    --------------   -------------------------
      6 Months           38, 13, 32, 35, 21
      12 Months          38, 44, 35, 48, 27
      18 Months          46, 15, 53, 51, 29
      24 Months          52, 29, 60, 44, 36

  
  
  - **(ii)** You are interested in determining if there is a difference in antibody levels at 1, 2, and 3 months post-treatment.

- **Solution:** 
  
  - (i) Here, 
    
    -Effect Size:  `\(f =\sqrt{\frac{(27.8−37.3)^2+(38.4−37.3)^2+(38.8−37.3)^2+(25.2−37.3)^2}{4}}/ 12.74 = 0.608\)`
    
    - To get sphericity, ran ANOVA
    
    
    ```r
    library(ez)
    ```
    
    ```
    ## Warning: package 'ez' was built under R version 4.1.3
    ```
    
    ```
    ## Registered S3 methods overwritten by 'car':
    ##   method                          from
    ##   influence.merMod                lme4
    ##   cooks.distance.influence.merMod lme4
    ##   dfbeta.influence.merMod         lme4
    ##   dfbetas.influence.merMod        lme4
    ```
    
    ```r
    data=data.frame(Patient= factor(rep(c(1,2,3,4,5),4)),
                    Month= factor(c(rep("6 Months",5),rep("12 Months",5),rep("18 Months",5),rep("24 Months",5))),
                    Serum= c(38,13,32,35,21,38,44,35,48,27,46,15,53,51,29,52,29,60,44,36))
    anova3= ezANOVA(data, dv=Serum, wid=Patient, within=.(Month),detailed=TRUE)
    anova3
    ```
    
    ```
    ## $ANOVA
    ##        Effect DFn DFd     SSn    SSd         F           p p<.05       ges
    ## 1 (Intercept)   1   4 27825.8 1506.7 73.872171 0.001006882     * 0.9212804
    ## 2       Month   3  12   706.6  870.9  3.245378 0.060146886       0.2291032
    ## 
    ## $`Mauchly's Test for Sphericity`
    ##   Effect         W         p p<.05
    ## 2  Month 0.1556327 0.4348287      
    ## 
    ## $`Sphericity Corrections`
    ##   Effect       GGe     p[GG] p[GG]<.05       HFe      p[HF] p[HF]<.05
    ## 2  Month 0.4844127 0.1187469           0.6892662 0.09014564
    ```
    
    - Note: [For more details about *ezANOVA() function* for Sphericity and Repeated Measures ANOVA ](https://people.umass.edu/bwdillon/LING609/Lectures/Section3/Lecture21.html)
    
    - Sphericity was non-significant (0.43), so coefficient of 1
    
    - One group, four measurements, within-effects so type 1
    
    - **R Code:**
    
    ```r
      print(paste0("The Sample Size is :",round(wp.rmanova(n=NULL, ng=1, nm=4, f=0.608, nscor=1, alpha=0.05, power=0.80, type=1)$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is :31"
    ```
    
  - (ii) You are interested in determining if there is a difference in antibody levels at 1, 2, and 3 months post-treatment.
      
      - Guess a nonsphericity correction of of 1 and medium effect 0.25
      
      - One group, three measurements, type 1
      
      - **R Code:**
    
    ```r
      print(paste("The Sample Size is :",round(wp.rmanova(n=NULL, ng=1, nm=3, f=0.25, nscor=1, alpha=0.05, power=0.80, type=1)$n,0)))
    ```
    
    ```
    ## [1] "The Sample Size is : 156"
    ```






