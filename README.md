### Jerry (Shien) Zhang

Data analyst and engineer in Toronto. BComp (Honours), Queen's University, 2026.

I build data pipelines and predictive models end to end. What I care about is
whether the numbers hold up when someone pushes on them — so most of what is
below ships with the checks, the failure cases, and the things that went wrong.

Currently looking for a full-time data role in the GTA.

---

#### Selected work

**[sql-data-warehouse](https://github.com/C0k11/sql-data-warehouse)** — A medallion
data warehouse in T-SQL on SQL Server: bronze → silver → gold, a Type-2 customer
dimension with hash-based change detection, and a gate of 40 declarative quality
checks that fails the pipeline rather than logging and moving on. Rebuilds 116,294
source rows from scratch in a container on every push. The README documents the
defects the checks caught, including one where every gender value in 18,483 rows was
silently corrupted while every domain check still passed.

**[credit-default-prediction](https://github.com/C0k11/credit-default-prediction)** —
Loan default risk on Home Credit data: 307,511 applicants, 58.1M rows across six
relational tables aggregated into behavioural features. LightGBM with controlled
same-fold experiments, so each gain is attributable — baseline 0.7586 → features
0.7852 → tuning 0.7889 OOF AUC, and 0.7852 on Kaggle's private leaderboard, which
means the validation was honest. SHAP for what actually drives risk.

**[stock-share-Helper](https://github.com/C0k11/stock-share-Helper)** (QuantAI) —
Portfolio analytics and decision support: a DuckDB + dbt star schema with 68
data-quality tests, 24 indicators and a Black-Scholes options engine, 748 pytest
checks, and a QLoRA-distilled local LLM analyst that only narrates numbers the
engine computed — never does the math itself.

**[game-ui-cv-agent](https://github.com/C0k11/game-ui-cv-agent)** — An end-to-end
computer-vision data pipeline: 47K frames collected, then narrowed to a 34K-image
labelled training set by automated dedup, train/val leakage detection and label
audits. Three YOLO detectors covering 455 classes; the UI model reaches 98.1% mAP50,
re-measured on the frozen deployed weights rather than read off a training log —
and on 129 of the 184 classes that actually have validation coverage, which the
README states outright rather than rounding into a headline number.

**[Conference-Database](https://github.com/C0k11/Conference-Database)** — A normalized
13-table MySQL schema with ISA subclassing and weak entities, plus an analytics query
pack (window functions, CTEs, anti-join audits) validated against a live database.

---

#### What I work with

`SQL Server / T-SQL` `Python` `dbt` `DuckDB` `MySQL` `pandas` `LightGBM`
`scikit-learn` `SHAP` `Tableau` `Docker` `GitHub Actions` `Git`

---

[Portfolio](https://personal-portfolio-jade-eta-20.vercel.app) ·
[LinkedIn](https://www.linkedin.com/in/jerryzhang-data) ·
shienzhang542@gmail.com
