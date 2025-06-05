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

	•	Profit increases with moderate discounts and peaks at d_min = 0.123, yielding a maximum profit of 13,558.84 PLN.
 
	•	Beyond this point, higher discounts reduce profit due to lower margins.
 
	•	Importantly, profit remains within 95% of the maximum when d_min lies between 0.106 and 0.18, offering a range of flexible yet effective pricing strategies.
 

