# A/B-тест: влияние вариантов оформления заказа на конверсию в покупку



## Источник данных и лицензия



Использован учебный синтетический датасет **Checkout A/B test** от **Datanemics**: одна строка соответствует одному пользователю, впервые увидевшему вариант оформления заказа. Датасет содержит 6 000 строк и 8 столбцов. Это искусственно созданные данные, не яыдяется результатом реального коммерческого эксперимента.

* [Страница датасета и описание полей](https://datanemics.com/datasets/ab-test-checkout/)
* [Скачать исходный CSV](https://datanemics.com/datasets/data/ab-test-checkout.csv)
* [Учебное задание к датасету](https://datanemics.com/blog/an-exercise-on-ab-test-checkout/)
* [Условия CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)

На странице датасета указана лицензия **CC0 1.0 Universal**. Она позволяет копировать, изменять и распространять данные, в том числе в публичном GitHub-репозитории и для коммерческих целей, без запроса разрешения. Указание авторства для датасета не требуется; ссылка на Datanemics приведена для прозрачности и воспроизводимости анализа. Условия источника проверены 4 ноября 2026 года.

Лицензия CC0 относится к исходному датасету. Расчёты, график и аналитические выводы подготовлены в рамках этого портфолио-проекта. Отдельная лицензия на авторские материалы проекта в этом README не назначается.



**Цель A/B-теста:** определить, повышают ли варианты оформления заказа A и B конверсию в покупку относительно текущего оформления — контрольной группы. Дополнительно сравнить денежные показатели без отдельной проверки их статистической значимости.



**Дизайн эксперимента:** в тесте участвовали 6 000 уникальных пользователей: контрольная группа — 1 974, группа A — 1 937, группа B — 2 089. Каждый вариант отдельно сравнивался с контрольной группой. Основной показатель — конверсия в покупку; дополнительные — выручка на пользователя и выручка на покупателя.



## Общие выводы



**Конверсия:** в контрольной группе — 8,87%, в группе A — 10,27%, в группе B — 11,63%. Прирост относительно контрольной группы составил +1,41 п.п. (+15,89%) для A и +2,77 п.п. (+31,21%) для B. Абсолютный и относительный прирост конверсии у B почти вдвое выше, чем у A.

**Статистическая значимость:** после поправки Бонферрони рост конверсии выявлен только у B: p-значение 0,19% ниже скорректированного порога 2,5%. У A p-значение составляет 6,71% — данных недостаточно, чтобы подтвердить рост. Скорректированный доверительный интервал B остаётся положительным: от +0,64 до +4,90 п.п. Интервал A — от −0,70 до +3,52 п.п. — включает ноль.

**Денежные показатели:** выручка на пользователя составила 5,68 $ в контрольной группе, 6,57 $ в группе A (+15,67%) и 8,43 $ в группе B (+48,41%). Относительный прирост у B примерно втрое выше, чем у A. Выручка на покупателя в B также выше контрольной группы на 13,10%, тогда как в A практически не изменилась (−0,19%). Денежные показатели поддерживают выбор B, однако статистическая значимость этих различий отдельно не проверялась.

**Динамика:** конверсия группы B выше контрольной группы в 18 из 28 дневных когорт, группы A — в 15 из 28. У B наблюдается общая тенденция к росту конверсии к концу периода, хотя дневные значения заметно колеблются. У A аналогичной восходящей тенденции не прослеживается.

**Ограничения:** при предполагаемом распределении 1:1:1 проверка распределения пользователей даёт p-значение 4,32% — немного ниже порога 5%. Однако реальный план распределения неизвестен, поэтому сначала нужно проверить запланированные доли.



## Бизнес-рекомендации

**Предварительно выбрать вариант B:** он сочетает статистически значимый рост конверсии, наиболее высокие наблюдаемые денежные показатели и преимущество по конверсии в большинстве рассмотренных дневных когорт.

До полноценного запуска проверить план распределения пользователей. Если планировались равные доли 1:1:1 — выяснить причину выявленного отклонения. Также отдельно оценить статистическую значимость прироста выручки на пользователя.

Затем внедрять B поэтапно, сохраняя контрольную группу и отслеживая конверсию и выручку на пользователя.

**Для внедрения A оснований недостаточно. A не внедрять.**



## Инструменты

Расчёты и график выполнены в Microsoft Excel.

---

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
