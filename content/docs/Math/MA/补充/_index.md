---
title: "补充资料"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}


# 函数空间定义与包含关系

| 符号 / 名称                            | 中文全称                 | 核心定义                                             | 判定关键                                                     | 典型函数示例                                  | 主要用途                     |
| -------------------------------------- | ------------------------ | ---------------------------------------------------- | ------------------------------------------------------------ | --------------------------------------------- | ---------------------------- |
| \\( \mathcal R[a,b] \\)                      | 黎曼可积函数             | 达布上下和确界相等，黎曼和极限存在                   | 有界 \+ 间断点为零测集                                       | 连续函数、单调函数、有限间断有界函数          | 定积分计算、经典微积分       |
| \\( C^0(\Omega) \\) / \\( C(\Omega) \\)            | 连续函数                 | 定义域内逐点连续                                     | \\( \varepsilon \\)\-\\( \delta \\) 极限等于函数值                       | 多项式、三角函数                              | 分析基础、介值/最值定理      |
| \\( C^k(\Omega) \\)                          | k阶连续可微函数          | 所有 \\( 1\sim k \\) 阶偏导数存在且连续                    | 求导后仍属 \\( C^0 \\)                                             | \\( x^2\in C^\infty \\)，\\( \|x\|\notin C^1 \\)            | 微分方程、泰勒展开           |
| \\( C^\infty(\Omega) \\)                     | 光滑函数 / 无穷次可微    | 任意阶偏导数都存在且连续                             | 对任意 k 都属于 \\( C^k \\)                                        | \\( e^x \\)、\\( \sin x \\)                               | 流形、分布理论               |
| \\( C_c^k(\Omega) \\)                        | 紧支集 \\(C^k\\) 函数          | \\( C^k \\) 且支集 \\( \operatorname{supp}f \\) 为紧集（有界闭） | 非零点闭包有界 \+ \\( C^k \\)                                      | bump 函数（截断光滑函数）                     | PDE 测试函数、分部积分消边界 |
| \\( C_c^\infty(\Omega) \\)                   | 紧支光滑函数（测试函数） | 紧支集 \+ 无穷光滑                                   | 同时满足 \\( C_c^k \\)（任意 k）                                   | mollifier 软化子                              | 分布论、广义函数基础         |
| \\( \mathrm{Lip} \\) / \\( \mathrm{Lip}^1 \\)      | Lipschitz连续函数         | \\( \|f(x)-f(y) \| \le L\|x-y\| \\)                              | 存在全局Lipschitz常数 L                                       | \\( C^1 \\) 有界导函数必 Lipschitz                  | 微分方程存在唯一性           |
| \\( \mathrm{Lip}^\alpha \\) / \\( C^{0,\alpha} \\) | Hölder 连续函数          | \\( \|f(x)-f(y)\|\le M\|x-y\|^\alpha,\ 0<\alpha\le1 \\)        | 存在指数 α 和常数 M                                          | \\( \|x\|^\alpha \\)（α\<1 时仅 Hölder 非 Lipschitz） | 正则性理论、Schauder 估计    |
| \\( BV[a,b] \\)                              | 有界变差函数             | 全变差 \\( \bigvee_a^b f < +\infty \\)                     | 分割变差上确界有限                                           | 单调函数、阶梯函数                            | 曲线长度、测度论             |
| \\( \mathcal L^1(\Omega) \\)                 | 勒贝格可积函数           | \\( \int_\Omega \|f\|\,d\mu < +\infty \\)                    | 绝对值积分有限                                               | 狄利克雷函数（L 可积但 R 不可积）             | 实分析、控制收敛定理         |
| \\( \mathcal L^p(\Omega) \\)                 | p次可积函数              | \\( \|f\|_p=\left(\int\|f\|^p\right)^{1/p}<\infty \\)        | p 次幂积分有限                                               | \\( p=2 \\) 平方可积（傅里叶核心）                  | 泛函分析、希尔伯特空间       |
| \\( \mathcal L^\infty(\Omega) \\)            | 本质有界函数             | 去掉零测集后全局有界                                 | 存在本质上确界 \\( \operatorname{ess\,sup} \\)                     | 有界可测函数                                  | 对偶空间、算子估计           |
| \\( W^{k,p}(\Omega) \\)                      | Sobolev 索伯列夫空间     | k 阶弱导数属于 \\( \mathcal L^p \\)                        | 分布意义下可导 \+ Lp 可积                                    | PDE 弱解                                      | 偏微分方程弱解理论           |
| \\( \mathcal S(\mathbb R^n) \\)              | 速降函数空间             | 函数及任意阶导数多项式速降                           | \\( \forall \alpha,\beta,\sup\|x^\alpha\partial^\beta f\|<\infty \\) | \\( e^{-\|x\|^2} \\) 高斯函数                         | 傅里叶变换封闭               |

**包含关系链（闭区间上）**：

\\( C_c^\infty \subset C^\infty \subset C^k \subset C^1 \subset \mathrm{Lip} \subset C^{0,\alpha} \subset C^0 \subset \mathcal R \subset \mathcal L^1 \\)

\\( \text{单调函数} \subset BV \subset \mathcal R \\)

> （注：部分内容可能由 AI 生成）