# Cheat-sheets
# 📚 Cheat Sheets

An interactive coding reference built from the **Bayesian Inference 2026** notebook. Covers every coded algorithm with line-by-line annotations, quick-reference tables, and a universal Bayesian recipe.

🔗 **[Live Site](https://yourusername.github.io/bayesian-cheatsheet)** ← replace with your URL

---

## What's Inside

| Section | Topic | Key Concept |
|---|---|---|
| 01 | Numerical Bayes | Grid → likelihood → normalize → plot |
| 02 | Beta-Bernoulli Updating | Conjugate closed-form update rule |
| 03 | MAP Estimation | argmax(log-likelihood + log-prior) |
| 04 | Non-Conjugate Prior | Bayes works numerically for any prior |
| 05 | Quick Reference | Every numpy/matplotlib function used |

---

## The Universal Bayesian Recipe

Every posterior in this notebook follows the same 3-line pattern:

```python
prior        = ...any function of theta...
unnormalized = likelihood(theta, data) * prior
posterior    = unnormalized / np.trapezoid(unnormalized, theta)
```

---

## Libraries Used

- `numpy` — grid, integration (`np.trapezoid`), log, argmax
- `matplotlib` — plotting, vertical lines (`axvline`), legends

---

## How to Use

Open `index.html` in any browser — no install needed. Use the nav pills at the top to filter by topic. Click **copy** on any code block to copy it directly.

---

## Topics Covered (from notebook)

- Bayes' theorem and the normalizing constant (evidence)
- Beta-Bernoulli conjugacy — update rule: `α += successes, β += failures`
- Posterior mean of Beta distribution: `α / (α + β)`
- MAP = MLE + regularization (Gaussian prior ↔ Ridge, Laplace ↔ Lasso)
- Numerical posterior when conjugacy doesn't apply
- Next steps: MCMC for high-dimensional posteriors
