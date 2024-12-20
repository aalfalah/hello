---
tag : 
- Tech/DAX
- Tech/Power_BI
---


In **information theory**, the **entropy** of a **random variable** quantifies the average level of uncertainty or information associated with the variable's potential states or possible outcomes. 

This measures the expected amount of information needed to describe the state of the variable, considering the distribution of probabilities across all potential states. 

Given a discrete random variable $X$ which takes values in the set $X$ and is distributed according to $p:X→[0,1]$, the entropy is


${\displaystyle \mathrm {H} (X)=-\sum _{x\in {\mathcal {X}}}p(x)\log p(x),}$

where $Σ$ denotes the sum over the variable's possible values.


This might seem quite unusual, but I personally had occasions where I used Entropy as a proxy to measure some aspects of users behaviour.

The following **DAX** code snippets are good examples of how to implement **Entropy** and use it in **Power BI**

``` SQL
ShannonEntropy =
	SUMX(
	ADDCOLUMNS(
		SUMMARIZE(
		'R01_Table',
		'R01_Table'[Value],
		"Probability",
		DIVIDE(
		COUNTROWS('R01_Table'),
		COUNTROWS(ALL('R01_Table'))
		)
		),
		"H(X)",
		-1 * [Probability] * LOG([Probability],2)
		),
	[H(X)]
	)
```


The previous snippets compute the overall entropy of the values in the column. To calculate the individual entropy of each distinct value, you can use the following DAX formula :


``` SQL
IndividualShannonEntropy =
	VAR __Probability =
		DIVIDE(
		COUNTROWS('R01_Table'),
		COUNTROWS(ALL('R01_Table'))
	)
	VAR __HX = -1 * __Probability * LOG(__Probability,2)
RETURN __HX
```