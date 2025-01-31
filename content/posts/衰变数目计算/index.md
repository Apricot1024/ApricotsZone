+++
date = '2024-06-15'
draft = false
description = '不稳定核的衰变数目计算关系'
title = '半衰期与衰变数目计算'
tags = ['Science', 'Concept']
# math = true
+++

# Lambda and T12

## 衰变概率
衰变常数可以用于描述原子核的衰变几率，表示单位时间内发生衰变的概率。
## 半衰期与衰变常数关系
根据半衰期的定义：
$$
N_t = N_0 \cdot 2^{-\frac{t}{T_{\frac 1 2}}}
$$


$$
\lambda = \frac{\mathrm{ln}(2)}{T_{\frac12}}
$$

## 活度与不稳定核数量
$$
A=-\frac{\mathrm d N}{\mathrm d t} = \lambda N
$$



# 数量计算
衰变常数: $\lambda$

0 时刻活度为 $A_0$

分支比为 $\epsilon$ ，能量为 $E$ 的伽玛测量计数为 $n$

测量时间为$t_1$ ~ $t_2$
## 活度积分
$t$ 时刻活度 $A$ 为：
$$
A = A_0 \cdot e ^ {- \lambda t}
$$

测量时间$t_1$ ~ $t_2$目标核衰变数量 $N_{measured}$ 为：
$$
N_{measured} = \int_{t_1} ^{t_2} A \mathrm dt,\\\
N_{measured} = \int_{t_1} ^{t_2} A_0 \cdot e ^ {- \lambda t} \mathrm dt,\\\
N_{measured} = \frac {A_0} {\lambda} \left (e ^{-\lambda t_1} - e ^{-\lambda t_2} \right ) 
$$

$E$ 处探测效率 $\eta$ 为：
$$
\eta = \frac {n}{N_{measured}\cdot \epsilon}
$$


## 数量衰变
0 时刻放射性核数目 $N_0$ 为：
$$ 
N_0 = \frac {A_0} {\lambda}
$$

$t_1$ 时刻衰变剩余 $N_{t_1}$ 为：
$$
N_{t_1} = N_0 e ^{-\lambda t_1}，\\\
N_{t_1} = \frac {A_0} {\lambda} e ^{-\lambda t_1}
$$

$t_2$ 时刻衰变剩余 $N_{t_2}$ 为：
$$
N_{t_2} = N_0 e ^{-\lambda t_2}，\\\
N_{t_2} = \frac {A_0} {\lambda} e ^{-\lambda t_2}
$$

测量时间$t_1$ ~ $t_2$目标核衰变数量 $N_{measured}$ 为：
$$
% N_{measured} = N_{t_1} - N_{t_2}\\
N_{measured} = \frac {A_0} {\lambda} e ^{-\lambda t_1} - \frac {A_0} {\lambda} e ^{-\lambda t_2}
$$

$E$ 处探测效率 $\eta$ 为：
$$
\eta = \frac {n}{N_{measured}\cdot \epsilon}
$$

## 其他
相同不稳定核，已知一片靶上活度，规避效率进行活度推算

测量开始时不稳定核数目：
$$
N_d = \frac{area}{\left(1-e^{-\lambda t}\right)\cdot \eta\cdot \varepsilon}
$$
可以从已知活度的样品抽取一个$k$，有级联加和时$k$仅与衰变核种类相关，规避含加和的效率问题。
$$
N_d = k \cdot \frac{area}{\left(1-e^{-\lambda t}\right)}, k=\frac{1}{ \eta\cdot \varepsilon}
$$
$$
k = \frac{N_d\cdot \left(1-e^{-\lambda t}\right)}{area}
$$
