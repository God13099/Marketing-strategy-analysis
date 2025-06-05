# Marketing-strategy-analysis
## Project Overview
### Organization Description

This project analyzes a medium-sized supermarket chain operating in a highly competitive retail market, offering fast-moving consumer goods (FMCG), with a focus on yogurt and fresh dairy products.

To remain competitive, especially during a 90-day shopping festival, the company uses discount-based promotional strategies to boost demand. During this period, retailers are expected to apply discounts, making pricing decisions especially critical.

Yogurt is highly price-sensitive, so finding the right minimum discount level is essential — low enough to maintain margins, but high enough to attract purchases. Excessive discounting can harm profitability or train customers to wait for sales.

This issue belongs to strategic pricing and promotion planning and focuses on how discount decisions affect sales and profit.The key challenge is to define a discount strategy that maximizes profit over the promotion period by accounting for customer responsiveness to prices and promotion dynamics.

### Problem Description

The company aims to determine the optimal minimum daily discount d_min to apply during a 90-day mandatory shopping festival, where competitors also offer promotional pricing. The goal is to maximize the total profit over the campaign.

The core decision variable is:
• d_min ∈ [0.01, 0.4] – the minimum discount level allowed.

Discounts beyond 40% reduce the product price below cost (5 PLN × (1 – 0.4) = 3 PLN), making the sale unprofitable.

Mathematical Representation:

![image](https://github.com/user-attachments/assets/cc97e3c1-309b-4817-8f78-414a3ba7083a)
Where:
![image](https://github.com/user-attachments/assets/a55085db-610f-43f4-a0d6-821a3e91a5c3)

Simulation Logic:

• On each day t ∈ [1, 90], demand is simulated using a price-sensitive exponential demand function.

• Sales are limited by available inventory.

• If units remain unsold, holding costs are incurred and next day’s demand is reduced.

• The discount level d_t is updated dynamically using a logistic function based on current sales.

### Analysis Results
#### Overview

<img width="256" alt="image" src="https://github.com/user-attachments/assets/5bfb9b41-542b-404f-ad25-d13c71d7806e" />

The Figure shows a clear nonlinear relationship:

•Profit increases with moderate discounts and peaks at d_min = 0.123, yielding a maximum profit of 13,558.84 PLN.
 
•Beyond this point, higher discounts reduce profit due to lower margins.
 
•Importantly, profit remains within 95% of the maximum when d_min lies between 0.106 and 0.18, offering a range of flexible yet effective pricing strategies.

#### Results Table
<img width="116" alt="image" src="https://github.com/user-attachments/assets/28626eda-5cea-468d-be70-a0a7cec168c5" />

<img width="230" alt="image" src="https://github.com/user-attachments/assets/2ff546db-92fa-4465-ad4e-2cc8c77904a7" />

we can draw the following conclusions：

Optimal Point: The fitted curve reaches its peak around d_min = 0.13, corresponding to the maximum profit of approximately 13000.

Curve Shape: The quartic fit captures a clear unimodal pattern—profit increases with d_min up to a point, then declines sharply, showing strong sensitivity beyond the optimum.

Downside Risk: Profit falls rapidly when d_min > 0.2, dropping below 10,000 at d_min = 0.27, and under 7,000 at d_min = 0.35, suggesting a steep loss in performance from over-discounting.

Stable Zone: The profit remains within 95% of the maximum (≥12,255) when d_min is in the range of approximately [0.106, 0.18], indicating a relatively robust optimal region. 

### Interpretation and Business Relevance

This outcome confirms a key managerial insight: moderate discounts (around 12%) are most effective at stimulating demand without sacrificing margin. Very small discounts fail to boost sales significantly, while excessive discounts harm profitability.

The identified range [0.106, 0.18] allows retailers to adapt within operational limits without risking significant financial loss. This supports data-driven decision-making for pricing during competitive campaigns, aligning well with intuitive promotional strategy: discount just enough to drive volume, but no more than necessary.


