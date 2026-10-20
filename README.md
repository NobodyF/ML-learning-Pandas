# Assignment #1 (demo). Exploratory data analysis with Pandas

| # | Question | Answer |
|---|----------|--------|
| 1 | Men and women in the dataset | Male: 21,790 · Female: 10,771 |
| 2 | Average age of women | 36.86 |
| 3 | Percentage of German citizens | 0.42% |
| 4 | Age of those earning >50K (mean / std) | 44.25 / 10.52 |
| 5 | Age of those earning ≤50K (mean / std) | 36.78 / 14.02 |
| 6 | Do all >50K earners have at least high school education? | No (HS-grad, 7th–12th etc. are also present) |
| 7 | Max age of Amer-Indian-Eskimo men | 82 |
| 8 | Share of >50K: married vs single men | Married 44.05% vs single 8.45% → married |
| 9 | Max hours/week, how many people, % >50K | 99 hours · 85 people · 29.41% |
| 10 | Avg hours/week in Japan (≤50K / >50K) | 41.00 / 47.96 |

# Assignment #2 (demo). Analyzing cardiovascular disease data

| # | Question | Answer |
|---|----------|--------|
| 1.1 | Men and women in the dataset | 45530 women and 24470 men (gender 1 = women, 2 = men) |
| 1.2 | Who more often reports consuming alcohol | Men (10.64% vs 2.55%) |
| 1.3 | Difference in % of smokers, men vs women | 20 (21.89% vs 1.79%) |
| 1.4 | Difference in median age (months), non-smokers vs smokers | 20 (657.4 vs 637.5) |
| 1.5 | CVD fraction ratio, smoking men 60–64 (ap_hi 160–180 & chol 3 vs ap_hi <120 & chol 1) | 3 (0.864 / 0.263 ≈ 3.28) |
| 1.6 | Correct BMI statements | 2 and 4 (women 27.99 vs men 26.75; healthy non-drinking men 25.87 vs women 26.85) |
| 1.7 | % of data filtered out | 10 (70000 → 63259) |
| 2.1 | Strongest Pearson correlation with gender | Height, Smoke (0.51, 0.34) |
| 2.2 | Strongest Spearman rank correlation | Ap_hi, Ap_lo (0.74) |
| 2.3 | Why the strong rank correlation | Nature of the data |
| 2.4 | Smallest age where CVD outnumbers non-CVD | 55 |

# Assignment #3 (demo). Decision trees with a toy task and the UCI Adult dataset

| # | Question | Answer |
|---|----------|--------|
| 1 | Entropy S0 of the initial system | 0.985 |
| 2 | Split by Looks_handsome: S1 / S2 / IG | 0.811 / 0.918 / 0.128 |
| 3 | Entropy of balls_left | 0.961 |
| 4 | Entropy of a fair die | 2.585 |
| 5 | IG from splitting balls into balls_left / balls_right | 0.161 |
| 6 | Test accuracy, tree max_depth=3 | 0.845 |
| 7 | Test accuracy, tree max_depth=9 | 0.848 (official answer; current sklearn gives 0.858) |
| – | Optional: RF 100 trees / tuned RF test accuracy | 0.853 / 0.865 |

# Assignment #4 (demo). Exploring OLS, Lasso and Random Forest in a regression task

| # | Question | Answer |
|---|----------|--------|
| 1 | Linear regression MSE (train / holdout) | 0.558 / 0.584 |
| 2 | Most influential feature (linear regression) | density |
| – | Least informative feature (Lasso, alpha=0.01) | fixed acidity, citric acid, total sulfur dioxide (all zeroed) |
| 3 | Least informative feature (tuned LassoCV) | citric acid |
| 4 | Tuned Lasso MSE (train / holdout) | 0.558 / 0.583 |
| 5 | Random Forest MSE (train / CV / holdout) | 0.053 / 0.414 / 0.372 |
| 6 | Tuned Random Forest MSE (CV / holdout) | 0.398 / 0.366 (best: max_depth=21, max_features=6) |
| 7 | Most important feature (Random Forest) | alcohol |

# Assignment #5 (demo). Logistic Regression and Random Forest in the credit scoring problem

| # | Question | Answer |
|---|----------|--------|
| 1 | Probability of correct majority verdict (5 jurors, 70% each) | 83.70% |
| 2 | 90% interval for mean age of customers who delayed repayment | 45.71 – 46.13 |
| 3 | Optimal C for logistic regression | 0.001 |
| 4 | Is the best model stable (std < 0.5%)? | std = 0.43% → Yes by the definition (official key says No) |
| 5 | Most important feature (scaled logistic regression) | NumberOfTime30-59DaysPastDueNotWorse |
| 6 | Softmax weight of DebtRatio | 0.11 |
| 7 | Change in odds of not repaying after +20 years of age | 0.70 (0.695) |
| 8 | ROC AUC gain of Random Forest over logistic regression | 0.04 computed (0.836 vs 0.796); official key: 0.03 |
| 9 | Weakest feature in Random Forest | NumberOfDependents |
| 10 | Main advantage of logistic regression over Random Forest | Feature interpretability |
| 11 | Best bagging ROC AUC | 80.93% computed → closest option 80.75% |
| 12 | Why these bagging max_features / max_samples are best | Less correlation between single models |

# Assignment #7 (demo). Unsupervised learning

| # | Question | Answer |
|---|----------|--------|
| 1 | Principal components needed for 90% variance | 65 |
| 2 | Variance covered by the first component | 51% |
| 3 | Clusters visible on the first two components | 2 clusters: (walking, upstairs, downstairs) and (sitting, standing, laying) |
| 4 | Activity best separated by KMeans | All three options are incorrect (best is walking upstairs, 0.80) |
| 5 | Number of clusters by the elbow method | 2 |
| 6 | Correct ARI statements | All three (KMeans ARI 0.42 < Agglomerative 0.49) |
| 7 | Best C for LinearSVC | 0.1 |
| 8 | Worst precision / recall for SVM | Precision – standing, recall – sitting |
| 9 | CV accuracy drop with PCA | 4% (0.938 vs 0.898) |
| 10 | Correct PCA statements | tSNE is better for visualization but PCA is cheaper; PCA components can be hard to interpret |