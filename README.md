# A/B Test: The Impact of Checkout Variants on Purchase Conversion



## Data Source and License



This project uses the educational synthetic dataset **Checkout A/B test** from **Datanemics**: each row represents one user exposed to a checkout variant for the first time. The dataset contains 6,000 rows and 8 columns. These are artificially generated data, rather than the results of a real commercial experiment.

* [Dataset page and field descriptions](https://datanemics.com/datasets/ab-test-checkout/)
* [Download the original CSV](https://datanemics.com/datasets/data/ab-test-checkout.csv)
* [Dataset exercise](https://datanemics.com/blog/an-exercise-on-ab-test-checkout/)
* [CC0 1.0 Universal terms](https://creativecommons.org/publicdomain/zero/1.0/)

The dataset page specifies the **CC0 1.0 Universal** license. It permits copying, modifying, and distributing the data, including in a public GitHub repository and for commercial purposes, without requesting permission. Attribution for the dataset is not required; the link to Datanemics is provided for transparency and reproducibility of the analysis. The source terms were checked on November 4, 2026.

The CC0 license applies to the original dataset. The calculations, chart, and analytical conclusions were prepared as part of this portfolio project. This README does not assign a separate license to the project's original materials.



**A/B test objective:** determine whether checkout variants A and B increase purchase conversion compared with the current checkout experience—the control group. Additionally, compare monetary metrics without separately testing their statistical significance.



**Experimental design:** the test included 6,000 unique users: 1,974 in the control group, 1,937 in group A, and 2,089 in group B. Each variant was compared separately with the control group. The primary metric was purchase conversion; additional metrics were revenue per user and revenue per buyer.



## Overall Conclusions



**Conversion:** 8.87% in the control group, 10.27% in group A, and 11.63% in group B. The increase relative to the control group was +1.41 percentage points (+15.89%) for A and +2.77 percentage points (+31.21%) for B. Both the absolute and relative conversion increases for B were almost twice those for A.

**Statistical significance:** after the Bonferroni correction, a statistically significant conversion increase was found only for B: its p-value of 0.19% was below the adjusted threshold of 2.5%. A's p-value was 6.71%, providing insufficient evidence to confirm an increase. B's adjusted confidence interval remained positive, ranging from +0.64 to +4.90 percentage points. A's interval, from −0.70 to +3.52 percentage points, included zero.

**Monetary metrics:** revenue per user was $5.68 in the control group, $6.57 in group A (+15.67%), and $8.43 in group B (+48.41%). B's relative increase was approximately three times A's. Revenue per buyer in B was also 13.10% higher than in the control group, while in A it was virtually unchanged (−0.19%). The monetary metrics support choosing B, although the statistical significance of these differences was not tested separately.

**Dynamics:** group B's conversion was higher than the control group's in 18 of the 28 daily cohorts, compared with 15 of 28 for group A. B showed an overall upward conversion trend toward the end of the period, although daily values fluctuated considerably. No similar upward trend was evident for A.

**Limitations:** under an assumed 1:1:1 allocation, the user allocation check yielded a p-value of 4.32%, slightly below the 5% threshold. However, the actual allocation plan is unknown, so the planned proportions must be verified first.



## Business Recommendations

**Provisionally select variant B:** it combines a statistically significant conversion increase, the highest observed monetary metrics, and a higher conversion rate than the control group in most of the daily cohorts examined.

Before a full rollout, verify the user allocation plan. If equal 1:1:1 proportions were planned, investigate the cause of the observed deviation. Also assess the statistical significance of the increase in revenue per user separately.

Then roll out B gradually, retaining a control group and monitoring conversion and revenue per user.

**There is insufficient evidence to roll out A. Do not roll out A.**



## Tools

The calculations and chart were created in Microsoft Excel.

