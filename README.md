# Hi, I'm Matin 👋

**Data Science student at Simon Fraser University | Python • SQL • Machine Learning • Data Analytics**

Objectivity and optimality are my work ethic.

I combine machine learning, database design, and statistical thinking with a bias toward one thing: finding what is actually true in the data, then turning that into a better decision. I am hardest on my own results, if a model looks too good, I go find out why before I trust it.

Currently preparing for Fall 2026 co-op roles in **Data Analysis, Data Science, Business Analysis, and Analytics Engineering**.

🔗 **Portfolio:** add-your-netlify-link-here

---

## What I work with

**Languages:** Python · SQL · R · C++ · Bash
**Data & ML:** pandas · NumPy · scikit-learn · statsmodels · XGBoost · Poisson & negative binomial regression · classification · model evaluation
**Visualization:** Matplotlib · Seaborn · Tableau · Excel
**Databases:** SQLite · relational database design · ER modeling · normalization · constraints · triggers
**Business skills:** stakeholder communication · decision support · operational analysis · documentation

---

## Projects I'm proud of

### MenuLens: menu decision analytics
**Should a restaurant cut a dish that still sells?**

A tool that scores every menu item on margin, prep time, demand trend, ingredient-waste risk, and **station pressure** (a feature I engineered as order volume × prep time to capture kitchen load), then recommends a clear action: keep, promote, reprice, or review for removal. Grounded in the Kasavana-Smith menu-engineering framework.

**What stands out:** a dish is only flagged for removal when low revenue **and** long prep **and** (thin margin **or** falling demand) line up, so the call is defensible, not a single-metric guess. I also caught my own bug, an early rule judged sales by unit count and flagged a top revenue earner to cut; switching to revenue contribution fixed it.

**Stack:** Python · pandas · Streamlit · feature engineering · rule-based decision logic · synthetic data
🔗 [Repo](https://github.com/MatinMeraj/menulens)

---

### ShiftCast: shift demand forecasting
**How many people should a shift be staffed for, when you can't know how busy it will be?**

Predicts customers (covers) per shift from things known in advance (day, shift, weather, events, prior week), then turns the forecast into a staffing number. The aim is to attack one lever behind kitchen turnover: overtime from understaffing.

**What stands out:** tested with a **time-based split** (train on the past, predict the future), not a random split that lets a model peek ahead. Started with Poisson, but the variance ran far above the mean (overdispersion, α ≈ 0.13), so a **negative binomial** fit best (R² ≈ 0.53, average error ≈ 28 covers). I also tried a Kalman time-series model as a cross-check; it beat a naive baseline but lost to the regression here, and I report that rather than crown the fancier model. Honest headline: about half of shift demand is predictable, so the right move is to staff that base and keep flexibility for the rest.

**Stack:** Python · pandas · statsmodels · Poisson / negative binomial regression · state-space (Kalman) · time-series validation · synthetic data
🔗 [Repo](https://github.com/MatinMeraj/shiftcast)

---

### MusicMood: audio vs. lyrics
**A song can sound like a party but read like a breakup.**

A team course project classifying songs into four moods using audio features and lyrics separately, then together. The motivation: streaming platforms tag mood mostly from sound, but a chill-sounding track can carry aggressive lyrics (think a diss track), so audio alone mislabels it.

**What stands out:** our early accuracy looked great until I traced it to **data leakage** and corrected it. The honest held-out results are audio **34.8%**, lyrics **36.1%**, and audio + lyrics fusion **41.5%**, against a **25%** random baseline for four classes. Fusing both sources beat either alone. The audit, and reporting the true number instead of the leaked one, is the part I'm proudest of.

**Stack:** Python · pandas · scikit-learn · VADER sentiment · feature engineering · confusion matrices · model evaluation
🔗 [Repo](https://github.com/MatinMeraj/Music-Mood-Classification)

---

### OverQualified: graduate underemployment (labour-market decision support)
Built a reproducible ML pipeline to predict graduate underemployment from structured survey data. Cleaned inconsistent categories, handled missing codes and class imbalance, and compared models with cross-validation.

**Result:** about **0.70 ROC AUC** with a tuned XGBoost pipeline (regularization, early stopping). A model like this could help career teams prioritize advising before underemployment becomes entrenched.

**Stack:** Python · pandas · scikit-learn · XGBoost · cross-validation · data cleaning
🔗 [Repo](https://github.com/MatinMeraj/Graduate-Underemployment-Prediction)

---

### Library Database: relational database + app
Designed and implemented a normalized library database (items, patrons, borrowing, events, personnel, room bookings, orders) with a Python application on top. Built the schema, enforced integrity with constraints and triggers, and validated it across **1,000+ records**.

**Result:** a clean, normalized structure (up to BCNF) that keeps data trustworthy from the start, supporting smoother borrowing workflows and faster reporting.

**Stack:** SQL · SQLite · Python · ER modeling · normalization · constraints · triggers
🔗 [Repo](https://github.com/MatinMeraj/library-database-app-)

---

## What I'm focused on now

Getting stronger at the full data workflow, not just modeling: ETL, pipelines, and computational data science, plus customer analytics and the difference between a business problem and an analytical problem (a model only matters if it answers the right question). I'm looking for Fall 2026 co-op and internship roles in data analytics, data science, business analysis, and analytics engineering.

---

## A bit more about me

- 🎓 BSc Data Science student at Simon Fraser University
- 💻 Associate Degree in Computer Science from Langara College
- 📊 Marketing Coordinator at the Data Science Student Society (DSSS)
- 🍳 Line cook in a high-volume kitchen (where a few of these project ideas started)
- 🤝 Open to co-op, internship, and project opportunities in data analytics and data science

---

## Let's connect

- **Portfolio:** add-your-netlify-link-here
- **LinkedIn:** [linkedin.com/in/matinmeraj](https://www.linkedin.com/in/matinmeraj)
- **GitHub:** [github.com/MatinMeraj](https://github.com/MatinMeraj)
- **Email:** matin_meraj_mohammadi@sfu.ca
