# Customer Lifetime Value (CLV) 

## Dataset Information:

This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

## Attribute Information:

* InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.

* StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.

* Description: Product (item) name. Nominal.

* Quantity: The quantities of each product (item) per transaction. Numeric.

* InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.

* UnitPrice: Unit price. Numeric, Product price per unit in sterling.

* CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.

* Country: Country name. Nominal, the name of the country where each customer resides.


## BG/NBD Model (with Gamma-Gamma extension)

BG/NBD stands for Beta Geometric/Negative Binomial Distribution.

### The BG/NBD model has few assumptions:

1. When a user is active, number of transactions in a time t is described by Poisson distribution with rate lambda.

2. Heterogeneity in transaction across users (difference in purchasing behavior across users) has Gamma distribution with shape parameter r and scale parameter a.

3. Users may become inactive after any transaction with probability p and their dropout point is distributed between purchases with Geometric distribution.

4. Heterogeneity in dropout probability has Beta distribution with the two shape parameters alpha and beta.

5. Transaction rate and dropout probability vary independently across users.

BG/NBD model can only be able to predict the future transactions and churn rate of a customer. It is then combined with the Gamma-Gamma model, which adds the monetary aspect of the customer transaction and we finally get the customer lifetime value (CLV).


### Some of the key assumptions of Gamma-Gamma model are:

1. The monetary value of a customer's given transaction varies randomly around their average transaction value.

2. Average transaction value varies across customers but do not vary over time for any given customer.

3. The distribution of average transaction values across customers is independent of the transaction process.


BG/NBD model can only be able to predict the future transactions and churn rate of a customer. It is then combined with the Gamma-Gamma model, which adds the monetary aspect of the customer transaction and we finally get the customer lifetime value (CLV).
