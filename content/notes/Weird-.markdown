+++
date = '2024-11-05T00:00:00-08:00'
draft = false
title = 'Weird Things in High Dimensions'
+++

Some weird stuff happens in high-dimensions. 

[Reference](https://x.com/aryehazan/status/1817877048053911912)


## 1. [High Dimensional Oranges Are Almost All Peel](https://x.com/tszzl/status/1817081479190708528)



Consider an $n$-dimensional cube of side length 1 containing a smaller $n$-dimensional cube with side length $0.8$ ("pulp") surrounded by a $0.1$-width border ("peel"). 

The volume of the pulp is $0.8^n$, which rapidly approaches 0 as $n$ increases:


| Dimensions | Pulp Volume ($0.8^n$) |
|------------|------------------------|
| 1          | 0.800                 |
| 2          | 0.640                 |
| 3          | 0.512                 |
| 5          | 0.328                 |
| 10         | 0.107                 |
| 20         | 0.012                 |
| 50         | 0.000014              |

[Another perspective](https://x.com/Jsevillamol/status/1817213852402303024): To randomly sample a point in this cube, we select $n$ independent coordinates from $[0,1]$. The point lies in the pulp only if all coordinates fall within $(0.1, 0.9)$. This probability is $(0.8)^n$, approaching 0 as $n$ increases.

In high dimensions, the volume is almost all in the surface.

## 2. Unit spheres get smaller in high dimensions
todo

This is very weird and requires non-trivial math to show.
[Wikepdia](https://en.wikipedia.org/wiki/Volume_of_an_n-ball)

[Good twitter post talking about this](https://x.com/RokoMijic/status/1818073988805152801)

[Drake](https://x.com/MaskedTorah/status/1818188397087015147) came up with a good explanation which is explained [here](https://x.com/RokoMijic/status/1818273024526733319)



## 3. [Spheres "spill out" in higher dimensions](https://stanislavfort.com/blog/sphere-spilling-out/)


## 4. Randomly chosen vectors in high-dimensional spaces are almost all orthogonal
The most intuitive explanation (in my opinion) is the probabilistic one.
Two vectors are orthogonal if their dot product is 0. 

$$
\langle x,y \rangle = \sum_{i=1}^n x_iy_i 
$$

Each $x_i$ and $y_i$ is randomly distributed from $[-1,1]$ which means that $\mathbb{E}[x_i y_i] = 0$ and the variance is proportional to $\frac{1}{n}$. This means that spread decreases with $n$.

When sampling only 2 or 3 times, the odds that you get a dot product close to 0 is not high, but because of the central limit theorem, sampling a lot means you almost always get really close to the mean.



## 5. Local minima are rare
todo


<!-- https://sites.astro.caltech.edu/~george/ay122/cacm12.pdf

> In high dimensions, most of the mass of a multivariate Gaussian distribution is not near the mean, but in an increasingly distant “shell” around it


> Naively, one might think that gathering more features never hurts, since at worst they provide no new information about the class. But in fact their benefits may be outweighed by the curse of dimensionality. -->

<!-- https://www.math.ucdavis.edu/~strohmer/courses/180BigData/180lecture1.pdf -->