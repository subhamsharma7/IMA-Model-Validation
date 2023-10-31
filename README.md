# IMA-Model-Validation
Advanced Approach under FRTB(IMA) requires institutions to meet quantitative tests namely Backtesting and PnL attribution..
In FRTB, there are two ways of calculating the market risk capital charge.
i) Standardised approach (SA) ii) Internal models approach (Advanced).

Q1) Well which method should we use?
Simple answer is less capital requirement under IMA makes it attractive.
But the other important factors are: a) The cost-benefit trade-off for each trading desk of doing IMA (versus doing SA only)
b) Whether the bank is willing to invest in an overall IT and process infrastructure that has the ability to support IMA calculations.

If banks want to use IMA then they need supervisory approval for each trading desk.
Now comes two statistical tests(Backtesting and Profit and Loss attribution) to help regulators to decide whether to make appointed desks to be eligible for IMA or not.

Backtesting: Done at both Bankwide(quarterly) and Trading desk level(daily)
Each trading desk must satisfy backtesting requirements on an ongoing basis to be eligible to use the IMA.

a) Backtesting requirements compare the value-at-risk (VaR) measure calibrated to a one-day holding period against each of the actual P&L (APL) and hypothetical P&L (HPL) over the prior 12 months.
The whole idea is that the maximum loss expectation at 1 day 99% VaR should be enough to cover loss figure given by APL and HPL.
An exception or an outlier occurs when either the actual or hypothetical loss of the trading desk registered in a day of the backtesting period exceeds the corresponding daily VaR measure determined by the bank’s model.

These number of exceptions are divided into three zones(outcome of Binomial distribution as each exceedancies follow bernouli distribution and sum of these exceptions follow binomial).

PLAT: Done at trading desk level for eligibility purpose
This is just a way of quantifying whether the risk models used to calculate risk capital requirement is in sync with the risk factors used in front office for PnL reporting.
It quantifies the accuracy of the risk models.

The PLA test compares daily risk-theoretical P&L (RTPL) with the daily HPL for each trading desk.
The RTPL is the daily trading desk-level P&L that is produced by the valuation engine of the trading desk’s risk management model.
The HPL must be calculated by revaluing the positions held at the end of the previous day using the market data of the present day (ie using static positions).

The PLA requirements are based on two test metrics:
(1) the Spearman correlation metric to assess the correlation between RTPL and HPL; and
(2) the Kolmogorov-Smirnov (KS) test metric to assess similarity of the distributions of RTPL and HPL.

Based on the outcome of the metrics, a trading desk is allocated to a PLA test red zone, an amber zone or a green zone.
