![Linear vs log–log](/assets/loglog_vs_linear.png)

Every log–log plot is a straight line, and I’m tired of pretending it isn’t.

This repository exists to stage a tiny visual trap in plain sight. The two panels above show the same synthetic dataset generated from a smooth, strictly positive, non-power-law function. Nothing dramatic changes between panels except coordinates. On linear axes, you see ordinary curvature and visibly uneven scatter. On log–log axes, the same points become suspiciously disciplined, as if the universe finally signed off on a scaling law. It did not. The geometry changed, not the mechanism.

The setup is intentionally boring. We start from an additive model, $y=f(x)+\varepsilon$, with $f(x)>0$ and noise $\varepsilon$ centered at zero. For small relative perturbations, a first-order expansion gives

$$\log y = \log(f(x)+\varepsilon) \approx \log f(x) + \frac{\varepsilon}{f(x)}.$$

That fraction is the entire trick. Log space turns absolute error into relative error by dividing by signal level. If $f(x)$ grows across decades of $x$, then the same additive noise contributes less visual vertical spread at larger $x$. The plot looks cleaner where the signal is large, even if the underlying additive uncertainty has not improved by a single bit.

Variance tells the same story with less poetry. Under the same small-noise approximation,

$$\mathrm{Var}(\varepsilon_{\log}) \approx \frac{\mathrm{Var}(\varepsilon)}{f(x)^2}.$$

So yes, uncertainty is compressed in log coordinates when $f(x)$ is large. This is mathematically legitimate and often useful, but it is also an invitation to over-interpret tidy-looking trends. A broad dynamic range plus coordinate compression can make mediocre structure look like deep law.

There is another subtlety: local elasticity. The quantity $d\log y / d\log x$ can drift slowly over a finite interval even when the global model is not a power law. In practice, that means a curved relationship can produce a log–log segment that appears almost straight over the exact range someone happened to plot. If the aesthetic reward is high enough, confirmation bias does the rest.

None of this is an argument against log transforms. They are essential in many domains, especially when multiplicative processes dominate or when dynamic ranges span orders of magnitude. The point is narrower and less glamorous: a straight-ish line on a log–log chart is a hypothesis prompt, not a conclusion. If the exponent matters, validate in original space, inspect residuals, compare alternative models, and check whether the governing physics actually predicts scaling. Otherwise, the clean line is mostly a coordinate artifact wearing a lab coat.

---
Filipe Borges
f3l5p7@yahoo.com.br
