+++
date = '2023-05-27T10:52:39+08:00'
draft = false
title = 'Reaction_rate'
tags = ['Science', 'Concept']
+++

- $$ r_{1,2}=N_{1} N_{2} \int_{0}^{\infty} v \sigma(E) P(E) \mathrm{d} E $$
- where N1 and N1 are the [number densities](../number_densities/index.md) of the two reacting particles in the plasma, v and E are, respectively, the relative velocity and energy of the particles, P (E)is the energy distribution and σ(E) is the cross section of the reaction as a function of the interaction energy.
- At typical stellar conditions the energy distribution of the interacting particles can be well approximated by a **Maxwell-Boltzmann distribution**. So:
- $$r_{1,2}=N_{1} N_{2}\left(\frac{8}{\pi \mu}\right)^{1 / 2} \frac{1}{k T^{3 / 2}} \int_{0}^{\infty} E \sigma(E) e^{-E / k T} \mathrm{~d} E$$
- Here T is the plasma temperature and μ is the reduced mass of the reacting particles.

在核天体物理中是联系微观和宏观的重要物理量，其截面(库仑势垒穿透系数)和粒子能量(麦克斯韦分布)分布预示着[[Gamow window]]，可以直接用于进行下一步天体环境发展的计算。
