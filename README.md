# Hi, I'm Eren

I build quantitative trading systems for prediction markets — probability modeling from first principles, market microstructure research, and low-latency execution. Python, asyncio, numpy; statistics hand-rolled rather than imported.

## What I've built

**🌡️ Polymarket weather-market trading system** *(private — write-up on request)*
Live system trading daily-high-temperature markets across ~28 cities. Bayesian inference engine (scalar Kalman filter over station temperature, Monte Carlo daily-max distributions, MDP decision layer) feeding a multi-VPS execution stack with a ~58 ms order fire path. Calibrated against realized outcomes across 28 markets. Found a real informational edge, traded it live, measured it honestly, and retired it when out-of-sample EV went negative.

**📉 Market efficiency study: Polymarket 5-minute BTC markets** *(private — write-up on request)*
Two-month market-making research program: Brownian-probit fair value, queue-position hazard models, regime-conditional EV, and a verification methodology built on placebo tests, chronological out-of-sample splits, and cluster bootstrap. Conclusion: the market is efficient at the retail-accessible level — and I can show exactly why.

## How I work

I model markets as MDPs the way physics uses free-body diagrams: first the qualitative philosophy of how the market actually works, then the MDP skeleton, then probability calculations from quality data to fill the chains. I kill my own models when the data says so.

🌐 [personal-website-new-phi-rose.vercel.app](https://personal-website-new-phi-rose.vercel.app) · 📫 erenege3500@gmail.com
