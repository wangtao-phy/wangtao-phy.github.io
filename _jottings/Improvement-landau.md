---
title: 对Landau绝热不变量引入的改进
date: 2026-04-16
---

Landau 引入绝热不变量时的讨论略有一些不直观，这里对其做一些改进，主要使用了全微分的一些性质。

考虑一个用哈密顿量 $H(q,p,\lambda)$ 刻画的系统，$\{q,p\}$ 是系统的广义坐标和广义动量，$\lambda$ 是引入的缓变参数。"缓变"本身是一个相对的概念，给出"缓变"的明确定义对于讨论是必要的。如果系统存在一个特征时间尺度 $T$，相对于该时间尺度的缓变可以表达为
{% raw %}
$$
T\frac{{\rm d}\lambda}{{\rm d} t}\ll\lambda.
$$
{% endraw %}
该等式的含义是，$\lambda$ 在该特征时间内的变化相对于 $\lambda$ 本身几乎可以忽略不计，"缓变"的意义通过这一比较明显体现出来。

在明确定义"缓变"后，可以区分哈密顿量的两种变化，一种是固定参数 $\lambda$ 的保守系统自身的变化，另一种是由 $\lambda$ 改变引起的变化。这里先考虑最一般的情况，哈密顿量的全微分为
{% raw %}
$$
{\rm d} H(q,p,\lambda)=\left(\frac{\partial H}{\partial q}\right)_{p,\lambda}{\rm d} q+\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}{\rm d} p+\left(\frac{\partial H}{\partial \lambda}\right)_{q,p}{\rm d} \lambda.
$$
{% endraw %}
因此如果考虑哈密顿量随时间的变化可得
{% raw %}
$$
\frac{{\rm d} H(q,p,\lambda)}{{\rm d} t}=\frac{{\rm d} q}{{\rm d} t}\left(\frac{\partial H}{\partial q}\right)_{p,\lambda}+\frac{{\rm d} p}{{\rm d} t}\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}+\frac{{\rm d}\lambda}{{\rm d} t}\left(\frac{\partial H}{\partial\lambda}\right)_{q,p}.
$$
{% endraw %}
考虑 $\lambda$ 无限缓慢地改变，那么可以认为每一时刻哈密顿方程仍近似成立
{% raw %}
$$
\frac{{\rm d} q}{{\rm d} t}=\left(\frac{\partial H}{\partial p}\right)_{q,\lambda},\quad\frac{{\rm d} p}{{\rm d} t}=-\left(\frac{\partial H}{\partial q}\right)_{p,\lambda}.
$$
{% endraw %}
在这一条件下，如果考虑的系统演化具有周期性，并将周期 $T$ 认为是上述特征时间尺度，那么
{% raw %}
$$
T=\int_{0}^{T}{\rm d} t=\oint\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}^{-1}{\rm d} q=-\oint\left(\frac{\partial H}{\partial q}\right)_{p,\lambda}^{-1}{\rm d} p.
$$
{% endraw %}
将无限缓慢条件下的哈密顿方程代入哈密顿量的时间导数便可以得到
{% raw %}
$$
\frac{{\rm d} H}{{\rm d} t}=\frac{{\rm d}\lambda}{{\rm d} t}\left(\frac{\partial H}{\partial\lambda}\right)_{q,p},
$$
{% endraw %}
对*周期运动*做平均得到
{% raw %}
$$
\overline{\frac{{\rm d} H}{{\rm d} t}}=\overline{\frac{{\rm d}\lambda}{{\rm d} t}}\ \overline{\left(\frac{\partial H}{\partial\lambda}\right)}_{q,p}.
$$
{% endraw %}
注意这里对周期运动做平均，因此认为 $\lambda$ 在周期内是近似不变的，其相对变化率也极小。但如果直接认为 {% raw %}${\rm d}\lambda/{\rm d} t${% endraw %} 为 0，则这一近似过于粗糙，退回到保守系统的情况，因此仍将其作为一个常数小量保留。作为一个常数小量，{% raw %}${\rm d}\lambda/{\rm d} t${% endraw %} 自然可以单独提出做平均。

对于由哈密顿量 $H(q,p,\lambda)$ 刻画的系统，独立变量应有 3 个 $\{q,p,\lambda\}$。如果从更一般的视角看，四个变量 $\{H,q,p,\lambda\}$ 任选其中 3 个作为独立变量都是允许的，例如有 $q(p,\lambda, H)$ 或 $p(q,\lambda, H)$。考虑 $p(q,\lambda, H)$（$q(p,\lambda,H)$ 同理，这里简单起见只讨论一种）的全微分得到
{% raw %}
$$
{\rm d} p(q,\lambda,H)=\left(\frac{\partial p}{\partial q}\right)_{\lambda,H}{\rm d} q+\left(\frac{\partial p}{\partial \lambda}\right)_{q,H}{\rm d} \lambda+\left(\frac{\partial p}{\partial H}\right)_{q,\lambda}{\rm d} H,
$$
{% endraw %}
将其代入哈密顿量的全微分得到
{% raw %}
$$
\begin{aligned}
{\rm d} H=&\left(\frac{\partial H}{\partial q}\right)_{p,\lambda}{\rm d} q+\left(\frac{\partial H}{\partial \lambda}\right)_{q,p}{\rm d} \lambda\\
&+\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}\left[\left(\frac{\partial p}{\partial q}\right)_{\lambda,H}{\rm d} q+\left(\frac{\partial p}{\partial \lambda}\right)_{q,H}{\rm d} \lambda+\left(\frac{\partial p}{\partial H}\right)_{q,\lambda}{\rm d} H\right].
\end{aligned}
$$
{% endraw %}
此时相当于将 $\{q,\lambda, H\}$ 作为独立变量讨论，三个微元各自变化等式应始终成立，这迫使三个微元的系数为 0，因此得到

$$
\begin{aligned}
0=&\left(\frac{\partial H}{\partial q}\right)_{p,\lambda}+\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}\left(\frac{\partial p}{\partial q}\right)_{\lambda,H},\\
0=&\left(\frac{\partial H}{\partial \lambda}\right)_{q,p}+\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}\left(\frac{\partial p}{\partial \lambda}\right)_{q,H},\\
0=&\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}\left(\frac{\partial p}{\partial H}\right)_{q,\lambda}-1.
\end{aligned}
$$

用对平均的定义重写前文的表达式，
{% raw %}
$$
\begin{aligned}
\overline{\frac{{\rm d} H}{{\rm d} t}}=&\overline{\frac{{\rm d}\lambda}{{\rm d} t}}\frac{1}{T}\int\left(\frac{\partial H}{\partial\lambda}\right)_{q,p}{\rm d} t\\
=&\overline{\frac{{\rm d}\lambda}{{\rm d} t}}\frac{1}{T}\oint\left(\frac{\partial H}{\partial \lambda}\right)_{q,p}\left(\frac{\partial H}{\partial p}\right)_{q,\lambda}^{-1}{\rm d} q\\
=&-\overline{\frac{{\rm d}\lambda}{{\rm d} t}}\frac{1}{T}\oint\left(\frac{\partial p}{\partial \lambda}\right)_{q,H}{\rm d} q.
\end{aligned}
$$
{% endraw %}
将周期 $T$ 的表达式代入整理得到
{% raw %}
$$
\oint\left[\left(\frac{\partial p}{\partial H}\right)_{q,\lambda}\overline{\frac{{\rm d} H}{{\rm d} t}}+\left(\frac{\partial p}{\partial\lambda}\right)_{q,H}\overline{\frac{{\rm d}\lambda}{{\rm d} t}}\right]{\rm d} q=0,
$$
{% endraw %}
因此得到系统存在一个近似不变量
{% raw %}
$$
\overline{\frac{{\rm d} I}{{\rm d} t}}=0,
$$
{% endraw %}
其中 $I$ 是沿着 $\lambda, H$ 给定的轨道的环路积分
{% raw %}
$$
I=\oint p{\rm d} q.
$$
{% endraw %}
这一推导过程利用多次利用了缓变作为近似条件，在"绝热"这一概念泛化为缓慢变化以后，将这一近似不变量称为"绝热不变量"也就不奇怪了。

本小节选择最简单的周期模型，给出了绝热所讨论的系统一个直观的图像。具体推导过程参考了Landau的力学教程，但对微元的分析做了优化，使变量间的关系更为清晰。将周期模型拓展到更一般的情况是该研究领域一直努力的方向，Krutkov在这一方向做出了重要贡献。
