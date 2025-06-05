# Marketing-strategy-analysis
## Project Overview
### Organization Description
This project analyzes a medium-sized supermarket chain operating in a highly competitive retail
market, offering fast-moving consumer goods (FMCG), with a focus on yogurt and fresh dairy
products.
To remain competitive, especially during a 90-day shopping festival, the company uses discount-based promotional strategies to boost demand. During this period, retailers are expected to apply discounts, making pricing decisions especially critical.
Yogurt is highly price-sensitive, so finding the right minimum discount level is essential — low enough to maintain margins, but high enough to attract purchases. Excessive discounting can harm profitability or train customers to wait for sales.
This issue belongs to strategic pricing and promotion planning and focuses on how discount decisions affect sales and profit.The key challenge is to define a discount strategy that maximizes profit over the promotion period by accounting for customer responsiveness to prices and promotion dynamics.
### Problem Description
The company aims to determine the optimal minimum daily discount d_min to apply during a 90-day
mandatory shopping festival, where competitors also offer promotional pricing. The goal is to
maximize the total profit over the campaign.
The core decision variable is:
• d_min ∈ [0.01, 0.4] – the minimum discount level allowed.
Discounts beyond 40% reduce the product price below cost (5 PLN × (1 – 0.4) = 3 PLN), making the sale unprofitable.
Mathematical Representation:
The objective is to maximize total profit:
Profitt = (pricet + reward) ⋅ 𝑞" − cost ⋅ demandt − holding_costt
Where:
• pricet = base_price × (1 − 𝑑")
• 𝑞" is the quantity sold, based on an exponential demand model with elasticity:
𝑞" ∼ PoissonBbase_demand ⋅ 𝑒#(%!&'.))D
The discount level is dynamically updated based on sales using a logistic function:
<img width="105" alt="image" src="https://github.com/user-attachments/assets/03e5f6c0-3d38-4686-9d8c-885ff59aedf0" />
