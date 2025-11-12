+++
date = '2024-11-28'
draft = true
title = 'Cu靶计算'
tags = ['Science', 'Activation']
+++

原天然铁19号靶中57Co活度为122Bq

预估65Zn的1115.5 keV效率为122 keV 的1/4，半衰期243.93d

活度达500Bq左右可达相似计数，且活度不确定度较小。

$$ 
N = \frac {A} {\lambda} = \frac{500 ~\mathrm{Bq}}{3.2888684507999854\times 10^{-8}\mathrm{s^{-1}}} = 15202797177.2
$$

4 MeV质子入射截面预计为$0.15 \mathrm{barns} = 1.5 \times 10^{-25} \mathrm{cm^2}$， 15小时1000enA流量估计

按公式
$$
N = \sigma T \Phi \frac{1-\mathrm e ^{-\lambda t}}{\lambda}
$$
$$
N = 1.5 \times 10^{-25}\times T\times\frac{1\times10^{-6}}{1.6\times10^{-19}}\times\frac{1-\mathrm{e}^{-3.2888684507999854e-08~\mathrm{s}^{-1}\times 15*3600}}{3.2888684507999854e-08~\mathrm{s}^{-1}}\\ = 5.058 \times 10^{-8} T
$$

为达到15202797177个剩余核，靶中65Cu的厚度至少为：
$$
T = 15202797177 \div 5.058 \times 10^{-8} = 3 \times 10^{17}
$$

65Cu在天然Cu中丰度30.8%，天然Cu靶厚：
$$
T = 3 \times 10^{17} \div 0.308 = 9.75 \times 10^{17} \mathrm{cm}^{-2}
$$
$$
T = \frac{9.75 \times 10^{17}}{6.02\times10^{23}}\times63500 = 0.103\mathrm{mg/cm^2}= 1.94*10^{-5}\mathrm{\mu g/cm^2}
$$

高截面靶厚衰减误差未考虑