---
title: Kendall Tau Rank Distance
tags: Algorithm theories
cover: 'https://s2.loli.net/2022/06/06/a5Uo1uDIX7W3H2v.jpg'
abbrlink: 51433
date: 2022-06-03 00:55:02
---

# Kendall Tau Rank Distance

There are many metrics to evaluate two rank list distances. The Kendall tau and Spearman's are classic metrics. They are comparably discussed in measurement [1].
As our XAI goal is to derive feature importance order and further evaluate the XAI methods results,
we have to assess the explanation consistency by measuring the distance between feature importance orders.

Kendall tau rank distance[1], is based on the Kendall tau rank correlation coefficient and can calculate the number of dissimilar between two rank lists.
The higher the Kendall tau number, the larger the distance, and the more disagreements the list has.
On the contrary, the smaller the number, the rank list shows higher similarity.
In detail, the Kendall tau rank correlation coefficient [2] is described as the equation and follows:

 \begin{equation}
 	\label{eq:ktrcc}
 	\tau\left(\sigma_{1}, \sigma_{2}\right)=\frac{2}{n *(n-1)}(|C|-|D|)
 \end{equation}
 where C is the set of concordant pairs, defined as:
 \begin{multline}
 	C= (i, j) \in S \times S \mid i<j \wedge(\sigma_{1}(i)<\sigma_{1}(j) \wedge   \\
 	\sigma_{2}(i)<\sigma_{2}(j) \vee
 	\sigma_{1}(i)>\sigma_{1}(j) \wedge \sigma_{2}(i)>\sigma_{2}(j)
 \end{multline}
 and D is the set of discordant pairs:
 \begin{multline}
 	D=(i, j) \in S \times S \mid i<j \wedge(\sigma_{1}(i)<\sigma_{1}(j) \wedge \\
 	\sigma_{2}(i)>\sigma_{2}(j) \vee \sigma_{1}(i)>\sigma_{1}(j) \wedge \sigma_{2}(i)<\sigma_{2}(j)
 \end{multline}

The Kendall tau rank distance is equal to $\frac{2}{n *(n-1)}$ if the two list are reversed. 
Otherwise, if the two lists are exactly the same, the value is zero. 

```python
import numpy as np

def normalised_kendall_tau_distance(values1, values2):
    """Compute the Kendall tau distance."""
    n = len(values1)
    assert len(values2) == n, "Both lists have to be of equal length"
    i, j = np.meshgrid(np.arange(n), np.arange(n))
    a = np.argsort(values1)
    b = np.argsort(values2)
    ndisordered = np.logical_or(np.logical_and(a[i] < a[j], b[i] > b[j]), np.logical_and(a[i] > a[j], b[i] < b[j])).sum()
    return ndisordered / (n * (n - 1))
```



[1]

V. A. Cicirello, “Kendall Tau Sequence Distance: Extending Kendall Tau from Ranks to Sequences,” *EAI Endorsed Transactions on Industrial Networks and Intelligent Systems*, vol. 7, no. 23, p. 163925, May 2020, doi: [10.4108/eai.13-7-2018.163925](https://doi.org/10.4108/eai.13-7-2018.163925).

[2]

V. A. Cicirello, “Kendall Tau Sequence Distance: Extending Kendall Tau from Ranks to Sequences,” *EAI Endorsed Transactions on Industrial Networks and Intelligent Systems*, vol. 7, no. 23, p. 163925, May 2020, doi: [10.4108/eai.13-7-2018.163925](https://doi.org/10.4108/eai.13-7-2018.163925).
