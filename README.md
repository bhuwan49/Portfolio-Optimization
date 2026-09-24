# Portfolio Optimization 


## Notation
- $N$: Number of assets
- $w$: Weight vector ($N \times 1$)
- $\mu$: Expected return vector ($N \times 1$)
- $\Sigma$: Covariance matrix ($N \times N$)
- $\iota$ (or $\mathbf{1}$): Vector of ones ($N \times 1$)
- $r_f$: Risk-free rate

---

## 1. Portfolio Expected Return
$$E(R_p) = w^T \mu$$

## 2. Portfolio Variance and Volatility
$$\sigma_p^2 = w^T \Sigma w$$
$$\sigma_p = \sqrt{w^T \Sigma w}$$

---

## 3. Global Minimum Variance (GMV) Portfolio
Finds the portfolio weights that minimize total risk without constraints on expected return.

**Weights:**
$$w_{gmv} = \frac{\Sigma^{-1} \iota}{\iota^T \Sigma^{-1} \iota}$$

---

## 4. Tangency Portfolio (Maximum Sharpe Ratio)
Maximizes the excess return per unit of total risk over the risk-free rate.

**Weights (unnormalized):**
$$w_{tan}^* = \Sigma^{-1} (\mu - r_f \iota)$$

**Weights (normalized to sum to 1):**
$$w_{tan} = \frac{\Sigma^{-1} (\mu - r_f \iota)}{\iota^T \Sigma^{-1} (\mu - r_f \iota)}$$

---

## 5. Mean-Variance Efficient Frontier
Minimizes portfolio variance for a target expected return ($R^*$):

$$\min_{w} \frac{1}{2} w^T \Sigma w$$

**Subject to:**
$$w^T \mu = R^*$$
$$w^T \iota = 1$$