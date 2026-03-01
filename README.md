![Linear vs log–log](/assets/loglog_vs_linear.png)

Every log–log plot is a straight line, and I’m tired of pretending it isn’t.

This figure is a small reality check: same data, same points, same noise, two different axis choices. On the left, linear axes show the curve for what it is, a smooth non-power-law trend with visibly uneven scatter. On the right, log-log axes politely iron out the drama and suggest a cleaner relationship than the data actually earned. If you squint long enough, everything starts to look like a scaling law, which is exactly how bad habits become conventions.

The setup is deliberately simple. Let the observed variable be y = f(x) + epsilon, where f(x) is the underlying smooth signal and epsilon is additive noise with mean zero. For positive y, a first-order expansion around f(x) gives log(y) = log(f(x) + epsilon) approximately log(f(x)) + epsilon / f(x), as long as |epsilon| / f(x) is small. That quotient is the trick. The same absolute perturbation gets divided by the local signal magnitude, so large f(x) regions absorb noise and look calm, while small f(x) regions keep more visible roughness. The plot did not become cleaner because physics got cleaner; it became cleaner because the coordinate transform rescaled the error.

This also shows up directly in variance. If epsilon_log denotes the transformed perturbation term, then Var(epsilon_log) approximately Var(epsilon) / f(x)^2 under the same small-noise assumption. In plain language, the vertical spread shrinks where the signal is large. A wide dynamic range plus a log transform is often enough to make random clutter look like disciplined structure. That can be useful for visualization, but it is not evidence by itself of a true power law.

So yes, use log-log plots when they help reveal multiplicative behavior or broad-scale trends. Just do not confuse geometric cosmetics with model validation. A straight-looking segment in transformed coordinates is a hypothesis generator, not a verdict. If the line matters, test the model in the original space, inspect residuals, and ask whether the mechanism truly implies scaling. Otherwise, congratulations: you successfully fit an optical illusion.

---
Filipe Borges
f3l5p7@yahoo.com.br
