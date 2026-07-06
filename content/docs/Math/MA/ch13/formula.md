---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据提供的源文件《第十三章 曲线积分与曲面积分》，现将其主要内容按照您要求的格式整理如下：

### 一、 定义汇总（按照“定义 13.x.x”形式整理）

*   **定义 13.1.1 (有界变差函数)**：设 \\( f \\) 为定义在 \\( [\alpha, \beta] \\) 中的函数。任给分割 \\( \pi: \alpha = t_0 < t_1 < t_2 < \dots < t_m = \beta \\)，记 \\( v(f; \pi) = \sum_{i=1}^m |f(t_i) - f(t_{i-1})| \\)。如果 \\( \sup_\pi v(f; \pi) \\) 有限，则称 \\( f \\) 为 \\( [\alpha, \beta] \\) 上的**有界变差函数**，其在 \\( [\alpha, \beta] \\) 中的全变差记为 \\( \bigvee_\alpha^\beta(f) = \sup_\pi v(f; \pi) \\)。
*   **定义 13.3.1 (面积公式)**：设 \\( \varphi: \Omega \rightarrow \mathbb{R}^n \\) 为非退化的 \\( C^1 \\) 映射，\\( \Omega \\) 为 \\( \mathbb{R}^m \\) 中可求面积的集合，则 \\( \varphi(\Omega) \\) 的面积定义为 \\( \sigma(\varphi(\Omega)) = \int_\Omega d\sigma = \int_\Omega \sqrt{\det[(J\varphi)^T J\varphi]} du_1 du_2 \dots du_m \\)。
*   **定义 13.3.2 (第一型曲面积分)**：设 \\( \varphi: \Omega \rightarrow \mathbb{R}^n \\) 为 \\( C^1 \\) 的参数曲面，\\( f \\) 是定义在此曲面 \\( \Sigma \\) 上的连续函数，则 \\( f \\) 在 \\( \Sigma \\) 上的**面积分**定义为 \\( \int_\Sigma f d\sigma = \int_\Omega f \sqrt{\det[(J\varphi)^T J\varphi]} du_1 du_2 \dots du_m \\)。
*   **定义 13.4.1 (第二型曲面积分)**：设 \\( \Sigma \\) 为 \\( \mathbb{R}^3 \\) 中的可定向曲面，\\( \varphi \\) 是与给定定向相容的参数表示：\\( \varphi(u, v) = (x(u, v), y(u, v), z(u, v)), (u, v) \in D \\)。对于定义在 \\( \Sigma \\) 上的连续向量值函数 \\( (P, Q, R) \\)，定义其曲面积分为 \\( \Phi = \int_D [P \frac{\partial(y,z)}{\partial(u,v)} + Q \frac{\partial(z,x)}{\partial(u,v)} + R \frac{\partial(x,y)}{\partial(u,v)}] du dv \\)，也记为 \\( \int_\Sigma P dy \wedge dz + Q dz \wedge dx + R dx \wedge dy \\)。

---

### 二、 公式汇总（按照原文序号整理）

*   **(13.1)**：\\( \int_\sigma f_1 dx_1 + f_2 dx_2 + \dots + f_n dx_n = \int_\alpha^\beta F(\sigma(t)) \cdot \sigma'(t) dt \\)
    *   **内容**：将第二型曲线积分转化为普通 Riemann 积分的计算公式。
*   **(13.2)**：\\( \sigma(\varphi(\Omega)) = \sqrt{\det[A^T A]} \sigma(\Omega) \\)
    *   **内容**：线性变换 \\( A \\) 作用下区域面积的变化比例。
*   **(13.3)**：\\( \sigma(\varphi(\Omega)) = \int_\Omega \sqrt{\det[(J\varphi)^T J\varphi]} du_1 du_2 \dots du_m \\)
    *   **内容**：\\( C^1 \\) 参数曲面面积的积分定义式。
*   **(13.4)**：\\( \sigma = \int_D \|r_u \times r_v\| du dv = \int_D \sqrt{EG - F^2} du dv \\)
    *   **内容**：\\( \mathbb{R}^3 \\) 中参数曲面面积的经典计算公式，其中 \\( E, F, G \\) 为第一基本形式系数。
*   **(13.5)**：\\( \sigma = \int_D \sqrt{1 + f_x^2 + f_y^2} dx dy \\)
    *   **内容**：函数图形 \\( z = f(x, y) \\) 形式的曲面面积公式。
*   **(13.6)**：\\( \sigma = \int_\Omega \|\varphi_{u_1} \times \varphi_{u_2} \times \dots \times \varphi_{u_{n-1}}\| du_1 du_2 \dots du_{n-1} \\)
    *   **内容**：超曲面面积的向量积表示。
*   **(13.7)**：\\( \sigma = \int_D \sqrt{1 + \|\nabla f\|^2} dx_1 dx_2 \dots dx_{n-1} \\)
    *   **内容**：高维超曲面图形的面积计算公式。
*   **(13.8)**：\\( \Phi = \int_\Sigma V \cdot \vec{n} d\sigma = \int_\Sigma V \cdot d\vec{\sigma} \\)
    *   **内容**：向量场流量（第二型曲面积分）的定义式。
*   **(13.9)**：\\( \Phi = \int_D [P \frac{\partial(y,z)}{\partial(u,v)} + Q \frac{\partial(z,x)}{\partial(u,v)} + R \frac{\partial(x,y)}{\partial(u,v)}] du dv \\)
    *   **内容**：第二型曲面积分在参数表示下的坐标计算式。
*   **(13.10)**：\\( \Phi = \int_\Sigma P dy \wedge dz + Q dz \wedge dx + R dx \wedge dy \\)
    *   **内容**：利用外微分形式表示的第二型曲面积分。
*   **(13.11)**：\\( f(x_1, x_2, \dots, x_n) - t = 0 \\)
    *   **内容**：用于推导余面积公式的水平集方程。
*   **(13.12)**：\\( x_n = \varphi_t(x_1, x_2, \dots, x_{n-1}) \\)
    *   **内容**：水平集方程的局部解形式。
*   **(13.13)**：\\( \nu(\Omega) = \int_a^b dt \int_{D \times \{t\}} \left| \frac{\partial f}{\partial x_n} \right|^{-1} dx_1 dx_2 \dots dx_{n-1} \\)
    *   **内容**：重积分变量替换推导余面积公式的中间步骤。
*   **(13.14)**：\\( \nu(\Omega) = \int_a^b dt \int_{f^{-1}(t) \cap \Omega} \frac{1}{\|\nabla f\|} d\sigma \\)
    *   **内容**：**余面积公式 (co-area formula)**，将重积分与第一型曲面积分联系起来。
*   **(13.15)**：\\( \nu(B_R) = \int_0^R \sigma(S_t) dt \\)
    *   **内容**：应用余面积公式，说明球体体积是球面积的积分。
*   **(13.16)**：\\( \int_{\partial D} \tilde{P} du + \tilde{Q} dv = \int_{\partial \Omega} P dx + Q dy \\)
    *   **内容**：第二型曲线积分在坐标变换下的不变性公式。
*   **(13.17)**：\\( \int_D (\frac{\partial \tilde{Q}}{\partial u} - \frac{\partial \tilde{P}}{\partial v}) du dv = \int_\Omega (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}) dx dy \\)
    *   **内容**：证明 Green 公式时，二重积分在坐标变换下的对应关系。
*   **(13.18)**：\\( \sigma(\Omega) = \frac{1}{2} \int_{\partial \Omega} x dy - y dx \\)
    *   **内容**：利用 Green 公式计算平面区域面积的公式。
*   **(13.19)**：\\( \int_{S^1} \frac{f dg - g df}{f^2 + g^2} = 0 \\)
    *   **内容**：特定全纯/调和条件下，沿圆周的积分值，用于证明代数基本定理。
*   **(13.20)**：\\( \int_\Omega (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}) v dx dy = \int_{\partial \Omega} v(P dx + Q dy) - \int_\Omega (Q \frac{\partial v}{\partial x} - P \frac{\partial v}{\partial y}) dx dy \\)
    *   **内容**：平面区域上的分部积分公式。
*   **(13.21) - (13.23)**：平面形式的 **Green 第一恒等式**，涉及 \\( \Delta u \\) 与法向导数 \\( \frac{\partial u}{\partial \vec{n}} \\) 的关系。
*   **(13.24)**：\\( \int_\Omega (v \Delta u - u \Delta v) dx dy = \int_{\partial \Omega} (v \frac{\partial u}{\partial \vec{n}} - u \frac{\partial v}{\partial \vec{n}}) ds \\)
    *   **内容**：平面形式的 **Green 第二恒等式**。
*   **(13.25)**：第二型曲面积分在空间坐标变换下的转换公式。
*   **(13.26)**：\\( \int_{\tilde{\Omega}} (\frac{\partial \tilde{P}}{\partial u} + \frac{\partial \tilde{Q}}{\partial v} + \frac{\partial \tilde{R}}{\partial w}) du dv dw = \int_\Omega (\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}) dx dy dz \\)
    *   **内容**：散度项在坐标变换下的不变性证明。
*   **(13.27)**：\\( \int_\Omega \text{div } X dx dy dz = \int_{\partial \Omega} X \cdot \vec{n} d\sigma \\)
    *   **内容**：**Gauss 散度定理**。
*   **(13.28) - (13.29)**：空间区域的分部积分公式。
*   **(13.30)**：\\( \int_\Omega v \Delta u dx dy dz = \int_{\partial \Omega} v \frac{\partial u}{\partial \vec{n}} d\sigma - \int_\Omega \nabla u \cdot \nabla v dx dy dz \\)
    *   **内容**：空间形式的 **Green 第一恒等式**。
*   **(13.31)**：\\( \int_\Omega (v \Delta u - u \Delta v) dV = \int_{\partial \Omega} (v \frac{\partial u}{\partial \vec{n}} - u \frac{\partial v}{\partial \vec{n}}) d\sigma \\)
    *   **内容**：空间形式的 **Green 第二恒等式**。
*   **(13.32)**：\\( \int_\Sigma \text{rot } X \cdot \vec{n} d\sigma = \oint_{\partial \Sigma} X \cdot T ds \\)
    *   **内容**：**Stokes 公式**，连接曲面积分与边界曲线积分。
*   **(13.33) - (13.34)**：涉及旋度和梯度的曲面分部积分与方向导数公式。
*   **(13.35) - (13.37)**：\\( \bigvee_a^b(f) = \bigvee_a^c(f) + \bigvee_c^b(f) \\) 及其相关变差不等式
    *   **内容**：描述全变差在区间上的可加性性质。