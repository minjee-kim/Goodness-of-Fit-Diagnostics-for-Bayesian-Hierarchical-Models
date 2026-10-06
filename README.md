# Goodness-of-Fit-Diagnostics-for-Bayesian-Hierarchical-Models
Notes and small illustrations around Yuan and Johnson, *Biometrics* 68(1):156–164, 2012. [PMC3276744](https://pmc.ncbi.nlm.nih.gov/articles/PMC3276744/) · [doi:10.1111/j.1541-0420.2011.01668.x](https://doi.org/10.1111/j.1541-0420.2011.01668.x)

This is not a reproduction of the paper. The paper checks a hierarchical model by evaluating a pivotal discrepancy measure at posterior draws and comparing it to a known reference distribution. These notes start from the fact that check uses.


## Examples

Run from the repository root. Figures are written to `figures/`.

| Script | What it shows |
| --- | --- |
| [`examples/01-pit.R`](examples/01-pit.R) | \(U = F(X)\) against uniform quantiles, for a correct \(F\) and a wrong scale |

```r
source("examples/01-pit.R")
```

`01-pit.R` draws \(n = 500\) and calls `qqplot` against `qunif(ppoints(n))`.

Correct transform, \(X \sim N(0,1)\), \(U = \Phi(X)\):

![Normal sample through the standard normal CDF](figures/01-pit-normal.png)

Correct transform for a second distribution, \(X \sim \mathrm{Exp}(1)\):

![Exponential sample through the exponential CDF](figures/01-pit-exp.png)

Same normal sample passed through \(\Phi(x/2)\). The scale is wrong, so the plot leaves the line:

![Normal sample through a CDF with the wrong scale](figures/01-pit-wrong-scale.png)

## Example 2

A three-covariate normal linear regression: simulate, take posterior draws of \((\beta, \sigma)\), apply the residual transform above to each draw, and QQ-plot against \(\mathrm{Uniform}(0,1)\).
