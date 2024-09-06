---
layout: post
title:  "Weird things in High Dimensions"
date:   2024-07-28
---

Some weird ass shit happens in high-dimensions. I wanted to keep track of some of them here

[Reference](https://x.com/aryehazan/status/1817877048053911912)


## 1. A high dimensional orange is mostly peel than pulp

Suppose you have an n-dimensional unit cube and the border has width 0.1. 
For n=2, the area of the pulp is $0.8^2 = 0.64$ $\text{units}^2$ and for n=3, the volume is $0.8^3 = 0.512$ $\text{units}^3$.
In n dimensions, the n-volume of the pulp is $0.8^n$ which goes to 0 and $n$ gets large. 

Another way to think about it from [this tweet](https://x.com/Jsevillamol/status/1817213852402303024) is picking random points from the cube and seeing how often they land near the edges. 
To pick a random point in an n-dimensional cube, we can independently pick $n$ coordinates from $[0,1]$ and if any of them happen to be in between $[0,0.1]$ or $[0.9,1]$ then they are in the peel (given the width is 0.1).
As $n$ gets large, the odds that at least one coordinate is on the edge gets larger with $n$.

The volume is almost all in the surface in high dimensions

## 2. The volume of n-dimensional unit spheres decreases with n when $n \geq 5$ 
This is very weird and not trivial to show.
[Wikepdia](https://en.wikipedia.org/wiki/Volume_of_an_n-ball)
[Good twitter post talking about this](https://x.com/RokoMijic/status/1818073988805152801)

Below is a picture from Wikipedia showing the n-volumes of balls from 0 to 25 dimensions

![Wikipedia](image.png)


## 3. Spheres "spill out" in higher dimensions
[Source](https://stanislavfort.com/blog/sphere-spilling-out/)

![high-dim-sphere](image-1.png)


## 4. Randomly chosen vectors in high-dim spaces are almost all orthogonal




## 5. Local minima are rare


