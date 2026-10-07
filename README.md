# Diagnosing the goodness of fit for Bayesian models 

Bayesian models, especially hierarchical models, offer a flexible framework for statistical inference. 
By allowing the users to incorporate prior information, accommodate complex dependence structures, and explicitly quantify uncertainty, Bayesian models offer substantial advantages in problems where conventional modeling assumptions may be restrictive.

However, this flexibility also presents challenges for model assessment. 
While advances in computational methods and statistical software have made Bayesian inference increasingly accessible, evaluating whether a fitted model adequately represents the observed data remains an essential and sometimes difficult task. 
This is particularly true for hierarchical models, where assumptions are introduced at multiple levels and model inadequacy may not be apparent from the posterior distribution alone.

A variety of Bayesian model-checking methods have been developed, including posterior predictive checks and diagnostics based on pivotal quantities. 
Nevertheless, these methods differ in their ability to detect model misspecification, and their implementation and interpretation require careful consideration. 
The availability of computational tools does not, by itself, establish the reliability of the resulting statistical inferences.

As Bayesian modeling becomes more accessible, there is increasing value in making model assessment equally accessible, systematic, and reproducible. 
The objective is not merely to obtain a posterior distribution, but to examine whether the assumptions underlying that distribution are reasonably supported by the data.

This collection of notes explores goodness-of-fit diagnostics for Bayesian models, with particular emphasis on hierarchical structures. 
Beginning with the framework developed by Yuan and Johnson (2012), it aims to provide intuitive explanations and practical illustrations of methods for detecting departures from model assumptions.



## Methodological Development

| Year | Reference | Main Idea |
| :--- | :--- | :--- |
| **2004** | **Johnson, V. E.** [*A Bayesian χ² test for goodness-of-fit*](https://doi.org/10.1214/009053604000000616). *The Annals of Statistics, 32*(6), 2361–2384. | Introduces a Bayesian goodness-of-fit test based on Pearson's chi-squared statistic, with a known asymptotic reference distribution. |
| **2007** | **Johnson, V. E.** [*Bayesian model assessment using pivotal quantities*](https://doi.org/10.1214/07-BA229). *Bayesian Analysis, 2*(4), 719–734. | Develops a general framework for model assessment using pivotal quantities evaluated at posterior draws. |
| **2012** | **Yuan, Y., & Johnson, V. E.** [*Goodness-of-fit diagnostics for Bayesian hierarchical models*](https://doi.org/10.1111/j.1541-0420.2011.01668.x). *Biometrics, 68*(1), 156–164. | Extends the framework to pivotal discrepancy measures, allowing assessment of model assumptions at multiple levels of a Bayesian hierarchy. |

## Notes and Illustrations

- **[Intuition](Intuition.qmd)** — Standardized residuals, probability integral transforms, and their role in Bayesian goodness-of-fit assessment.



