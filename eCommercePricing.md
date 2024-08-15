# E-commerce Pricing 
## Introduction 
A new online grocery shop has asked you to build a checkout and pricing process that they can use to calculate: 

how much they should charge for a given item to make a specific revenue amount. 
the final shopping cart value given a list of items and relevant discount codes. 
The shop owners have already hired a team to build the website and only require you to build a service that the website team can call. 

The list of products that the grocery shop will sell at launch is listed below: 

| Item name | Cost value | % Revenue | Tax  |
|-----------|------------|-----------|------|
| Lettuce   | £0.32      | 15%       | 20%  |
| Tomato    | £0.52      | 15%       | 20%  |
| Chicken   | £2.15      | 20%       | 20%  |
| Bread     | £1.55      | 15%       | 15%  |
| Jam       | £3.26      | 20%       | 15%  |
 
To calculate the price per unit cost (the price displayed on the website) the Cost value, % Revenue and Tax values are used. The final value is rounded up to the nearest pence. As an example, a lettuce will have a price per unit of £0.45 (£0.32 x 1.15 x 1.20 = £0.4416 which when rounded up is £0.45). 

The shopping cart total is calculated by adding together all the unit costs for items within a cart. To follow financial regulations the amount of tax that a customer is paying needs to be shown separately. As an example, if a customer buys a Lettuce and a Chicken the shopping cart value would be £3.55 of which £0.60 is tax (the pre-tax and post-tax price of a lettuce is £0.37 and £0.45 respectively and the pre-tax and post-tax price of a chicken is £2.58 and £3.10, respectively. Therefore, the total cost is £3.10 + £0.45 = £3.55 and the pre-tax cost is £0.37 + £2.58 = £2.95. The tax amount is £3.55 - £2.95 = £0.60). 

Your task is to build an API that the team building the website can call to return either a price per unit cost for a specific item or the total cost and tax amount of a given list of items making up a shopping cart. 

## Input 
For the price per unit cost, you will be provided with a single item name. 

For the shopping cart price, you will be provided with a comma separated list. Each element in the list will be formed of an integer value followed by the item name. Each item name will only appear once in the list. 

## Output 
For the price per unit cost a string rounded up to 2 decimal points should be provided 

For the shopping cart price two values need to be provided. The first, labelled as “total price” needs to be the full price of the cart including all taxes rounded to 2 decimal places. The second, labelled as “tax” need to be the amount of tax being paid rounded to 2 decimal places.  

Price per unit test Input: 

Jam 

Price per unit test expected Output: 

4.50 

Shopping cart test input: 

3 Tomato, 1 Chicken, 2 Bread 

Shopping cart expected output: 

total price 9.36, tax 1.40 