# Advising Company X on Sales Strategy

We are tasked with reviewing sales data corresponding to a firm we will refer to as Company X, and leveraging that sales data to assess the state of Company X's sales and make recommendations where possible.
We have two different datasets on hand in the form of Microsoft Excel (.xslx) files. The file top200_SKUs.xlsx contains sales data on the 200 best-selling products for each of the 39 regions which Company X divides Mexico into. The file ventas2017_2022.xlsx, on the other hand, contains the monthly sales history from January 2017 to December 2022 for each of the 39 regions.


# Recommendations for Further Analysis

In this analysis, our use of unsupervised machine learning methods allowed us to spot a handful of patterns concerning the distribution of SKU sales in different regions. Our use of time-series modeling, on the other hand, allowed us to anticipate how much in sales Company X would likely expect to be able to make in a given month, several months in advance, as well as suggesting that the collapse in sales in December 2022 is likely the result of an exogenous shock.

However, it seems to us that the main benefit of this analysis has been to identify what needs to be looked into in order to improve sales, rather than coming upon any particular strategy to do so. Exactly what particular strategy to boost sales will be most effectve requires we understand the SKUs in play more in-depth. For example, if it turns out that the SKUs in Cluster 3 have low margins, a strategy to offer discounts on these items might boost sales but could turn out to be highly unprofitable. A strategy to bundle SKU_162 with other SKUs might be a waste of time if SKU_162 turns out to be an item that is only relevant in certain zones/contexts.

If we were working with or at Company X, we would want to get our hands on information relating to SKU product categories, profit margins, as well as any historical information of demand elasticities by zone in order to understand the potential impact of any one strategy on a given category of SKUs. We should also try to understand the nature of the (likely) exogenous shock to sales the company suffered in December 2022. If a competitor undercut the company on price in an end-of-year sale, the company should think of what it can do to avoid the same situation next year. If the shock came as a result of regulatory changes or the entry of a new player into the market with significant competitive advantages, Company X might have to review its overall strategy.

