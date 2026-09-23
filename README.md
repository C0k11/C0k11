<a href="https://personal-portfolio-jade-eta-20.vercel.app">
  <picture>
    <source media="(prefers-reduced-motion: reduce)" srcset="assets/banner-still.png">
    <img src="assets/banner.webp" alt="Jerry Zhang, data and ML engineer, Toronto" width="100%">
  </picture>
</a>

I'm Jerry (Shien) Zhang, a data and ML engineer in Toronto. BComp (Honours), Queen's University, 2026.

I build data pipelines and predictive models end to end. What I care about is
whether the numbers hold up when someone pushes on them - so most of what is
below ships with the checks, the failure cases, and the things that went wrong.

Currently looking for a full-time data or ML role in the GTA.

---

#### Selected work

**[vlm-product-attributes](https://github.com/C0k11/vlm-product-attributes)** - Product type,
color and material from product photos with a LoRA-tuned Qwen3.5-4B, returned as JSON. On a
leak-checked, hash-frozen test split of 5,437 Amazon listings, fine-tuning lifts photo-only
accuracy from 0.70 / 0.72 / 0.80 to 0.86 / 0.79 / 0.88. A CLIP linear probe is a tough
baseline: the model beats it on color and ties on the rest, and the README says so. Served
with vLLM on one RTX 4090, going from 23 to 64 images/s on the val split after a shorter
prompt, a merged adapter and FP8 weights (FP8 costs 0.65 points on color).

**[sql-data-warehouse](https://github.com/C0k11/sql-data-warehouse)** - One warehouse
spec, built twice: T-SQL on SQL Server and PySpark + Delta Lake, the second running
unchanged on a laptop, in CI, and on Databricks. A Type-2 customer dimension with
hash-based change detection, and a gate of 40 declarative quality checks that fails
the pipeline rather than logging and moving on. The reason to build it twice is that
the two can be diffed - a parity harness compares 296 measurements across 11 tables
and they match exactly, so "the migration changed no data" is a test result rather
than a claim. The README documents the defects the checks caught, including one where
every gender value in 18,483 rows was silently corrupted while every domain check
still passed.

**[credit-default-prediction](https://github.com/C0k11/credit-default-prediction)** -
Loan default risk on Home Credit data: 307,511 applicants, 58.1M rows across six
relational tables aggregated into behavioural features. LightGBM with controlled
same-fold experiments, so each gain is attributable - baseline 0.7586 -> features
0.7852 -> tuning 0.7889 OOF AUC, and 0.7852 on Kaggle's private leaderboard, which
means the validation was honest. SHAP for what actually drives risk. The final
model is served as a scoring API on AWS Lambda behind API Gateway, deployed by
GitHub Actions with no stored keys.

**[stock-share-Helper](https://github.com/C0k11/stock-share-Helper)** (QuantAI) -
Portfolio analytics and decision support: a DuckDB + dbt star schema with 68
data-quality tests, 24 indicators and stats, a Black-Scholes options engine, 790+
pytest checks, and a QLoRA-distilled local LLM analyst that only narrates numbers the
engine computed - never does the math itself. The weekday pipeline also runs on AWS
Lambda, S3 and EventBridge Scheduler with CloudWatch alarms, and the same dbt project
runs on Snowflake from S3 Parquet, where all 68 tests pass and 36,277 mart rows match
DuckDB cell by cell.

**[game-ui-cv-agent](https://github.com/C0k11/game-ui-cv-agent)** - An end-to-end
computer-vision data pipeline: 47K frames collected, then narrowed to a 34K-image
labelled training set by automated dedup, train/val leakage detection and label
audits. Three YOLO detectors covering 455 classes; the UI model reaches 98.1% mAP50,
re-measured on the frozen deployed weights rather than read off a training log -
and on 129 of the 184 classes that actually have validation coverage, which the
README states outright rather than rounding into a headline number.

**[Conference-Database](https://github.com/C0k11/Conference-Database)** - A normalized
13-table MySQL schema with ISA subclassing and weak entities, plus an analytics query
pack (window functions, CTEs, anti-join audits) validated against a live database.

---

#### What I work with

`Python` `SQL Server / T-SQL` `Snowflake` `PySpark` `Delta Lake` `Databricks` `dbt`
`DuckDB` `MySQL` `pandas` `LightGBM` `scikit-learn` `SHAP` `PyTorch` `QLoRA` `vLLM`
`AWS` `Terraform` `Docker` `GitHub Actions` `Power BI` `Tableau` `Git`

---

[Portfolio](https://personal-portfolio-jade-eta-20.vercel.app) -
[LinkedIn](https://www.linkedin.com/in/jerryzhang-data) -
shienzhang542@gmail.com
