---
title: Square roots
---

# Square roots

_This article appeared first on my previous blog on december 2016_

Have you ever wondered what is behind the `sqrt()` function? In many cases, but not all there 
is an algorithm that is much older than the first computer: the newton method.
It is an iterative algorithm that "improves" the approximation of a variable x in the equation at each cycle:

<img src="https://latex.codecogs.com/gif.latex?x%5E2%20%3D%20a"/>


Where do you know `a`. For example, setting `a = 25` we obtain that `x² = 25`, and with a short
elementary calculation that `x² = 5`. Let's say we don't know how
to calculate the square root, we can then randomly pull and measure the error 
committed, this leads us to a form of the function:

<img src="https://latex.codecogs.com/gif.latex?x%5E2&plus;e%20%3D%20a" />

With each iteration of the algorithm, we want the error to decrease, so we iterate until `e` it is
not "small" enough (`e <0.00001`). We now need a function to calculate the "attempt" `x`.
This is given by the formula:

<img src="https://latex.codecogs.com/gif.latex?x_1%20%3D%20%5Cfrac%7B1%7D%7B2%7D%20%28x_k&plus;%5Cfrac%7Ba%7D%7Bx_k%7D%29" />

With `x_k` current attempt and `x_1` new attempt to evaluate.

