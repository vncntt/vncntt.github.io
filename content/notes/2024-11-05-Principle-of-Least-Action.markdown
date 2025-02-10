---
layout: post
title:  "Principle of Least Action"
date:   2024-11-05
---

I thought [this video](https://www.youtube.com/watch?v=Q10_srZ-pbs) was really fun and wrote up some of the derivations that the video went over quickly.

# Introduction and Basic Principles

Maupertuis' principle of least action states that the action, defined as:

$$
S_0 = \sum mvs
$$

where $m$ is the mass, $v$ is the velocity, and $s$ is the distance, reaches a minimum along the actual path of motion.

Euler later generalized this to a continuous form:

$$
S = \int mv ds
$$

This formulation holds only for systems with constant energy.

Consider a true path $x(t)$ and a nearby path $x(t) + \eta(t)$, where $\eta(t)$ is a small perturbation. 
Similar to how, at the minimum, of a parabola if you move a small distance the value of the function doesn't change much, you can show that the actions of these 
two paths are the same up to first order in  $\eta$.

As with any minimum, the first-order variation in the action vanishes:

$$
\delta S = 0
$$

where $\delta S$ represents the first variation of the action functional (some theorem in calculus of variations).

# Full Derivation of Lagrangian Equation

Starting from 

$$
\delta S = 0
$$
with 
$$
S = \int mv ds
$$
, we get 

$$
\delta \int mv ds = 0.
$$

Using $v = \frac{ds}{dt}$, 

$$
\delta \int m v^2 dt = 0.
$$

Since kinetic energy is $T = \frac{1}{2} mv^2$, 

$$
\delta \int 2T dt = 0.
$$

We also know that the total energy $E = T + V$ which means 

$$
\delta \int (T - V + E) dt = 0.
$$

which splits into

$$
\delta \int (T - V) dt + \delta \int E dt = 0.
$$

Since energy is constant, 

$$
\delta \int (T - V) dt + \delta(Et)= 0.
$$

Applying the variation product rule:

$$
\delta \int (T - V) dt + E \delta t + t \delta E = 0.
$$

Euler showed that:
1. Energy is constant along each path ($t \delta E = 0$)
2. We only consider paths with equal duration ($E \delta t = 0$)

Therefore:

$$
\delta \int (T - V) dt = 0.
$$

This is Hamilton's principle, where $L = T - V$ is the Lagrangian:

$$
\delta \int L dt = 0.
$$

# Deriving $F=ma$

Consider a path $y(t)$ with perturbation $\eta(t)$, giving $q(t) = y(t) + \eta(t)$. The action variation is:

$$
\delta S = S[q(t)] - S[y(t)]
$$

Computing the action for both paths:

$$
\begin{align*}
S[q(t)] = \int_{t_1}^{t_2} \left( \frac{1}{2} m \left( \frac{dy}{dt} \right)^2 - V(y) \right) \, dt + \int_{t_1}^{t_2} \left( m \frac{dy}{dt} \frac{d\eta}{dt} - \eta V'(y) \right) \, dt
\end{align*}
$$

$$
S[y(t)] = \int_{t_1}^{t_2} \left( \frac{1}{2} m \left( \frac{dy}{dt} \right)^2 - V(y) \right) \, dt
$$

After cancellation, we get

$$
\delta S = \int_{t_1}^{t_2} \left( m \frac{dy}{dt} \frac{d\eta}{dt} - \eta V'(y) \right) \, dt
$$
which doing some integration by parts (also using something called variation must vanish at endpoints) gives us 

$$
\delta S = \int_{t_1}^{t_2} \left( -m \frac{d^2y}{dt^2} - \frac{dV}{dy} \right) \eta dt = 0
$$

Since $\eta$ is arbitrary, we must have:

$$
m \frac{d^2y}{dt^2} = -\frac{dV}{dy}
$$

which, voila, is just  $F = ma$  which is Newton's second law. 

## Show how Euler-Lagrange's Equation implies Fermat's Principle of Least Time
todo
## Write out the Lagrangian for a double pendulum
todo