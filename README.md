# Parameter Estimation of Fee Process

The key question is whether the fee process is diffusive (as geometric Brownian motion) or confined to lie within a band around an average, which results from the mean-reverting process.

Although there is not enough fee history to answer this question conclusively, we have found that a unit root/Dickey-Fuller test (essentially a modified t-test) indicates that mean-reversion is significant at confidence levels & 85% (> 95% for the Canadian conduits and _ 85% for Old Line and Thunder Bay).

The resulting parameters, although some are poorly determined, indicate that the process reverts very quickly to a stationary process as one would expect. In this case, considering values of the reversion speed within a 95%-ile confidence band produces unrealistic long-term volatilities. We provide a more consistent estimate of parameter uncertainties based on an analysis of the fees as a stationary process.

Given the strong quantitative evidence from three conduits and strong qualitative evidence from all conduits, we are confident that the fee processes mean-revert in a way that is inconsistent with a geometric Brownian motion assumption.

We are interested in parameter estimation and model selection issues, which ultimately impact
on the expected loss calculations.

We will give an outline of the methodology employed to estimate parameters, and comment on the robustness of the results. We also provide a more realistic methodology for choosing a conservative parameter set.

The fee process is modeled as the continuous-time, mean-reverting process, where the Rt are related to the fee process ft by: ft = exp(Rt). If we introduce:


Using this, one finds the expected fee at time t given the initial fee f0 at t = 0:

In these, we have defined the asymptotic volatility as. Over times smaller than the reversion speed a (that is, when at _ 1), the solution (5) is approximately

so that ft is approximately a Geometric Brownian motion process with drift μ−R0. Note that if 1/a _T, where T is the time over which one is projecting the fee process, then the process would be described quite well be Brownian motion alone–without mean reversion.

In the other limit: at _ 1, the ‘mean reversion’ effect becomes clear by taking y _ 0 in (6) and (7):

Note that unlike geometric Brownian motion, both of these are static quantities–not only does the mean fee revert to a constant level, but the variation of the fee process around the asymptotic mean has a fixed ‘width’ given (roughly) by _1. Therefore, if we are interested in projecting the fee process to regimes where at _ 1, we may as well model it as a stationary process:

so that every month the fee is expected to be f1 with a spread given roughly by _1.


References:

https://finpricing.com/lib/FxForwardCurve.html

https://derivatives.hcommons.org/currency-products/
