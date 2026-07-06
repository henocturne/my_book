---
title: "definition"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}

根据源文件《第十三章 曲线积分与曲面积分》，该章节定义并使用了大量关于曲线、曲面、场论以及 Riemann-Stieltjes 积分的数学符号。以下是分类总结：

### 1. 曲线与第一型曲线积分符号
*   **\\( \sigma(t) = (x(t), y(t)) \\) 或 \\( (x_1(t), \dots, x_n(t)) \\)**：表示一条参数曲线。
*   **\\( L(\sigma) \\)**：表示曲线 \\( \sigma \\) 的**长度**。
*   **\\( \pi: \alpha = t_0 < t_1 < \dots < t_m = \beta \\)**：表示对区间 \\( [\alpha, \beta] \\) 的一个**分割**。
*   **\\( \|\pi\| \\)**：分割 \\( \pi \\) 的**模**（即子区间长度的最大值），常用于定义极限。
*   **\\( s(t) = L(\sigma|_{[\alpha, t]}) \\)**：**弧长函数**，表示曲线从起点到参数 \\( t \\) 处的长度。
*   **\\( ds = \|\sigma'(t)\| dt \\)**：**弧长微元**。
*   **\\( \int_{\sigma} f ds \\)**：函数 \\( f \\) 在曲线 \\( \sigma \\) 上的**第一型曲线积分**（或标量曲线积分）。

### 2. 第二型曲线积分符号
*   **\\( \int_{\sigma} F \cdot dx \\)** 或 **\\( \int_{\sigma} f_1 dx_1 + \dots + f_n dx_n \\)**：向量场 \\( F \\) 沿曲线 \\( \sigma \\) 的**第二型曲线积分**（或向量曲线积分）。
*   **\\( \oint_{\sigma} \\)**：沿**闭曲线（环路）**的积分符号。
*   **\\( dx = (dx_1, dx_2, \dots, dx_n) \\)**：微分向量。

### 3. 曲面与第一型曲面积分符号
*   **\\( \varphi: \Omega \rightarrow \mathbb{R}^n \\)**：参数曲面映射。
*   **\\( \sigma \\) 或 \\( \sigma(\varphi(\Omega)) \\)**：表示曲面的**面积**。
*   **\\( E, F, G \\)**：第一基本形式的系数，定义为 \\( E = r_u \cdot r_u, F = r_u \cdot r_v, G = r_v \cdot r_v \\)。
*   **\\( d\sigma \\)**：**面积微元**（标量），在参数表示下 \\( d\sigma = \|N\| du dv \\)。
*   **\\( N = \varphi_u \times \varphi_v \\)**：曲面的**法向量**。
*   **\\( \int_{\Sigma} f d\sigma \\)**：**第一型曲面积分**。

### 4. 第二型曲面积分符号
*   **\\( \vec{n} = (\cos \alpha, \cos \beta, \cos \gamma) \\)**：曲面的**单位法向量**，其中 \\( \alpha, \beta, \gamma \\) 为与坐标轴的夹角。
*   **\\( d\vec{\sigma} = \vec{n} d\sigma \\)**：**有向面积元**，常记作 \\( (dy \wedge dz, dz \wedge dx, dx \wedge dy) \\)。
*   **\\( \Phi = \int_{\Sigma} V \cdot d\vec{\sigma} \\)**：向量场 \\( V \\) 穿过曲面 \\( \Sigma \\) 的流量，即**第二型曲面积分**。

### 5. 场论算子与区域符号
*   **\\( \Omega \\) 与 \\( \partial\Omega \\)**：通常 \\( \Omega \\) 表示一个区域，\\( \partial\Omega \\) 表示其**边界**。
*   **\\( \nabla f \\)**：函数 \\( f \\) 的**梯度**。
*   **\\( \text{div } X \\)**：向量场 \\( X \\) 的**散度**。
*   **\\( \text{rot } X \\) 或 \\( \text{curl } X \\)**：向量场 \\( X \\) 的**旋度**。
*   **\\( \Delta u = \text{div}(\nabla u) \\)**：**Laplace 算子**。
*   **\\( \frac{\partial u}{\partial \vec{n}} \\)**：函数 \\( u \\) 沿法方向 \\( \vec{n} \\) 的**方向导数**。

### 6. Riemann-Stieltjes 积分与有界变差符号
*   **\\( v(f; \pi) = \sum |f(t_i) - f(t_{i-1})| \\)**：函数 \\( f \\) 关于分割 \\( \pi \\) 的**变差**。
*   **\\( \bigvee_a^b(f) \\)**：函数 \\( f \\) 在区间 \\( [a, b] \\) 上的**全变差**。
*   **\\( BV[a, b] \\)**：在 \\( [a, b] \\) 上所有**有界变差函数**构成的集合。
*   **\\( U(f, \alpha; \pi) \\) 和 \\( L(f, \alpha; \pi) \\)**：关于函数 \\( \alpha \\) 的 **Darboux 上和与下和**。
*   **\\( \int_a^b f(x) d\alpha(x) \\)**：函数 \\( f \\) 关于 \\( \alpha \\) 的 **Riemann-Stieltjes 积分**。
*   **\\( f \in \mathcal{R}(\alpha) \\)**：表示 \\( f \\) 关于 \\( \alpha \\) 是 Riemann-Stieltjes **可积的**。