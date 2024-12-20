---
tag : 
- DAX
- Power_BI
---

The funnel drop-off rate is a commonly used metric in e-commerce, especially for web-based purchasing processes involving a shopping cart. These processes typically consist of several steps for a customer to complete a purchase. For instance, the customer adds desired products to their shopping cart, reviews the cart, and proceeds to checkout. The checkout process may include entering payment details and additional information like a shipping address, followed by confirming the purchase. At any stage in this journey, a customer might abandon the process, resulting in a drop-off.

Analysing the funnel drop-off rate helps pinpoint specific steps where customers disengage, highlighting areas for improvement. The following examples demonstrate how to calculate the funnel drop-off rate in an e-commerce purchasing flow involving a shopping cart and payment. However, these methods can be applied to analyse any multi-step customer engagement process.

``` SQL
R01_Table =
UNION(
ADDCOLUMNS(
GENERATESERIES(1,10000,1),
"Page",
"Product",
"Step",
1
),
ADDCOLUMNS(
GENERATESERIES(1,7000,1),
"Page",
"Add to Shopping Cart",
"Step",
2
),
ADDCOLUMNS(
GENERATESERIES(1,2000,1),
"Page",
"Payment",
"Step",
3
),
ADDCOLUMNS(
GENERATESERIES(1,1200,1),
"Page",
"Confirmation",
"Step",
4
)
)
```



``` sql
Drop Off Rate =
VAR __CurrentStep = MAX([Step])
VAR __PreviousStep = __CurrentStep - 1
VAR __CurrentCount = COUNTROWS('R01_Table')
VAR __PreviousCount =
IF(
__CurrentStep = 1 ,
0 ,
COUNTROWS(FILTER(ALL('R01_Table'),[Step] =
__PreviousStep ))
)
RETURN
DIVIDE(__CurrentCount - __PreviousCount, __PreviousCount, 0)
```


The terms **funnel drop-off rate** and **funnel abandonment rate** are often used interchangeably. This metric can be calculated using two different approaches. The first method, as previously explained, involves determining the percentage of customers at a specific step who fail to progress to the next step. The second method calculates the percentage of customers who started the process but did not reach each subsequent step along the way. The following example illustrates how to compute this second version of the funnel drop-off rate:



``` sql
Abandonment Rate =
VAR __CurrentStep = MAX([Step])
VAR __PreviousStep = 1
VAR __CurrentCount = COUNTROWS('R01_Table')
VAR __PreviousCount =
COUNTROWS(FILTER(ALL('R01_Table'),[Step] = __PreviousStep ))
RETURN
DIVIDE(__CurrentCount - __PreviousCount, __PreviousCount, 0)
```