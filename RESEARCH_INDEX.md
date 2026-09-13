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

The public package covers Brownian-probit market pricing, binary inventory accounting, queue/fill
assumptions, EV decomposition and controlled policy experiments under the historical point-settlement
mechanism. Its deeper methods and estimator coverage are being expanded from the original research.

[Research repository](https://github.com/ErenEgeCelik/btc-5m-market-microstructure) ·
[Working paper](https://github.com/ErenEgeCelik/btc-5m-market-microstructure/blob/main/paper/manuscript.md)

Pricing-fit quality, forward prediction, modeled policy results and realized trading outcomes are
different claims. The paper and repository identify their data windows, measurement units and
evaluation status. Historical findings are not presented as a current tradable edge.

## Using this record

For a research or engineering application, select the contribution relevant to the role and attach
its implementation or experiment link. Preserve the method's scope: implemented software,
recomputed historical scores, fitted comparisons and trading outcomes are not interchangeable.
Numerical statements should retain their sample unit and model version.

My planned machine-learning and AI work is a future direction; it is separate from the completed
work indexed here. New projects will be added when there is an inspectable research record.

[Website](https://www.erenege.dev) · [Writing](https://www.erenege.dev/writing)
