# Research evidence index

I am an independent researcher working on quantitative trading. This index connects the methods,
implementations and empirical findings in my two published research programmes.

## Weather prediction markets

**Question:** How should station observations and forecasts change outcome probabilities and the
value of an action through an order book?

| Contribution | Technical evidence |
|---|---|
| Forecast-pulled temperature-state estimation; source noise and bias; Monte Carlo daily maxima | [Model equations and versions](https://github.com/ErenEgeCelik/weather-market-research/blob/main/docs/model-derivation.md) |
| Current, next-report and conditional outcome distributions linked to portfolio decisions | [Model-to-decision walkthrough](https://github.com/ErenEgeCelik/weather-market-research/blob/main/examples/decision_walkthrough.py), [payoff and decision equations](https://github.com/ErenEgeCelik/weather-market-research/blob/main/docs/decision-implementation.md) |
| Sensor information studies, ablations, calibration and historical probability evaluation | [Experiment records](https://github.com/ErenEgeCelik/weather-market-research/blob/main/docs/experiments.md), [runnable score audit](https://github.com/ErenEgeCelik/weather-market-research/blob/main/examples/research_audit.py) |
| Source-specific collection, concurrent scheduling and observation identity | [Acquisition implementation](https://github.com/ErenEgeCelik/weather-market-research/blob/main/docs/acquisition-implementation.md) |
| Cached metadata, pre-signing, preparation/submission separation and latency instrumentation | [Execution engineering](https://github.com/ErenEgeCelik/weather-market-research/blob/main/docs/execution-engineering.md), [measurement case](https://github.com/ErenEgeCelik/weather-market-research/blob/main/benchmarks/README.md) |

[Contribution IDs and application wording](https://github.com/ErenEgeCelik/weather-market-research/blob/main/CONTRIBUTIONS.md) ·
[Machine-readable contributions](https://github.com/ErenEgeCelik/weather-market-research/blob/main/evidence/claim_ledger.json) ·
[Reproduction commands](https://github.com/ErenEgeCelik/weather-market-research/blob/main/REPRODUCIBILITY.md)

The decision implementation is a one-step mean-variance evaluator. Historical collection, inference
and execution versions are identified separately. The experiment records distinguish fitted
comparisons, leave-one-day-out feature analysis, source-substituted replay and journal diagnostics.

## BTC five-minute up/down markets

**Question:** How do short-horizon information, book response, queue access and inventory exposure
combine into a market-making decision?

| Contribution | Technical evidence |
|---|---|
| Brownian-probit price construction; feed/anchor diagnostics; constant and feature-dependent scales; hybrid offset states | [Model equations and versions](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/market-pricing-model.md), [estimation method](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/pricing-estimation.md) |
| Archived scale-feature analysis with explicit feature availability and model-selection boundaries | [358-row study and figure](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/data/pricing/README.md), [runnable pricing audit](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/examples/pricing_walkthrough.py) |
| Causal feed/book alignment, recorder health, queue access, metadata caching and submission timing | [Data and execution engineering](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/data-engineering.md), [queue mechanics](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/queue-and-fill-mechanics.md) |
| Feed-to-book direction, timing, confirmation and saturation measurements | [Market response](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/market-response.md), [aggregate audit](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/estimators/mechanics_audit.py) |
| Split-inventory accounting, joint-fill outcomes, conditional drift and book-priced one-step EV | [EV derivation](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/mdp-ev-chain.md), [policy implementation](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/src/btc5m_research/policy.py) |
| Inventory and directional policy variants, paired output comparisons and execution diagnostics | [Strategies and results](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/strategies.md), [368-slot paired audit](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/estimators/policy_audit.py) |

[Contribution IDs and application wording](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/CONTRIBUTIONS.md) ·
[Machine-readable claims](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/evidence/claim_ledger.yaml) ·
[Reproduction commands](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/REPRODUCIBILITY.md)

The [binary-risk derivation](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/docs/binary-risk-and-market-making.md)
connects the Brownian model to terminal Bernoulli inventory risk and explains the Avellaneda–Stoikov
comparison. Its exact CARA diagnostic is publication exposition; the historical implementation
uses book-priced one-step EV with inventory rules, not a solved Bellman or A-S optimizer.

Pricing fit, forward prediction, modeled policy gains and realized trading outcomes are different
claims. The experiment records preserve sample units, versions, model-selection limitations and
replay assumptions under historical point settlement. The expanded working paper integrates these
methods, numerical comparisons and limitations:
[manuscript](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/paper/manuscript.md) /
[PDF](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/paper/crypto-working-paper.pdf).

Stable release reference: [crypto research expansion, September 2026](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/tree/6db010205b3aa3b8b4ee1d5715e06c47de8023b7).

## Using this record

For a research or engineering application, select the contribution relevant to the role and attach
its implementation or experiment link. Preserve the method's scope: implemented software,
recomputed historical scores, fitted comparisons and trading outcomes are not interchangeable.
Numerical statements should retain their sample unit and model version.

My planned machine-learning and AI work is a future direction; it is separate from the completed
work indexed here. New projects will be added when there is an inspectable research record.

[Website](https://www.erenege.dev) · [Writing](https://www.erenege.dev/writing)
