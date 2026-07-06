---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}


根据源文件《第十一章 多元函数的微分》，按照您的要求对公式和定义进行整理如下：

### 一、 定义整理

*   **定义 11.1.1 (方向导数)**：设 \\( D \subset \mathbb{R}^n \\) 为开集，\\( f: D \rightarrow \mathbb{R} \\) 为 \\( D \\) 中定义的函数。对于 \\( x^0 \in D \\)，以及 \\( \mathbb{R}^n \\) 中单位向量 \\( u \\)，如果极限 \\( \lim_{t \rightarrow 0} \frac{f(x^0 + tu) - f(x^0)}{t} \\) 存在，则称 \\( f \\) 在 \\( x^0 \\) 处沿方向 \\( u \\) **可导**，此极限称为 \\( f \\) 沿 \\( u \\) 的**方向导数**。
*   **定义 11.1.2 (微分)**：设 \\( D \subset \mathbb{R}^n \\) 为开集，\\( f: D \rightarrow \mathbb{R} \\) 为多元函数，\\( x^0 \in D \\)。如果存在线性映射 \\( L: \mathbb{R}^n \rightarrow \mathbb{R} \\)，使得在 \\( x^0 \\) 附近成立 \\( f(x) - f(x^0) = L(x - x^0) + o(\|x - x^0\|) \\)，则称 \\( f \\) 在 \\( x^0 \\) 处**可微**，\\( L \\) 称为 \\( f \\) 在 \\( x^0 \\) 处的**微分**，记为 \\( df(x^0) \\)。
*   **定义 11.3.1 (向量值函数的微分)**：设 \\( D \subset \mathbb{R}^n \\) 为开集，\\( f: D \rightarrow \mathbb{R}^m \\) 为向量值多元函数，\\( x^0 \in D \\)。如果存在线性映射 \\( L: \mathbb{R}^n \rightarrow \mathbb{R}^m \\)，使得在 \\( x^0 \\) 附近成立 \\( f(x) - f(x^0) = L(x - x^0) + o(\|x - x^0\|) \\)，则称 \\( f \\) 在 \\( x^0 \\) 处**可微**。
*   **定义 11.6.1 (极值)**：设 \\( D \subset \mathbb{R}^n \\)，\\( f: D \rightarrow \mathbb{R} \\) 为多元函数，\\( x^0 \in D \\)。如果存在 \\( \delta > 0 \\)，使得 \\( f(x^0) \ge f(x) \\)（或 \\( f(x^0) \le f(x) \\)），\\( \forall x \in D \cap B_{\delta}(x^0) \setminus \{x^0\} \\)，则称 \\( x^0 \\) 为 \\( f \\) 的**极大（小）值点**，\\( f(x^0) \\) 为 \\( f \\) 的**极大（小）值**。
*   **定义 11.6.2 (凸函数)**：设 \\( D \subset \mathbb{R}^n \\) 为凸集，\\( f: D \rightarrow \mathbb{R} \\) 为多元函数。如果任意 \\( x \neq y \in D \\)，均有 \\( f(tx + (1-t)y) \le tf(x) + (1-t)f(y) \\)，\\( \forall t \in (0, 1) \\)，则称 \\( f \\) 为 \\( D \\) 中的**凸函数**。

---

### 二、 公式整理

#### §11.1 方向导数和微分
*   **(11.1)**：\\( \frac{\partial f}{\partial u}(x^0) = df(x^0)(u) \\) —— **可微函数方向导数与微分的关系**。
*   **(11.2)**：\\( \nabla f(x^0) = (f_{x_1}(x^0), f_{x_2}(x^0), \dots, f_{x_n}(x^0)) \\) —— **梯度的定义**。
*   **(11.3)**：\\( df(x^0)(v) = \nabla f(x^0) \cdot v \\) —— **微分的梯度表示**。

#### §11.2 切线和切面
*   **(11.4)**：\\( N_i = (-1)^{i-1} \frac{\partial(x_1, \dots, x_{i-1}, x_{i+1}, \dots, x_n)}{\partial(u_1, u_2, \dots, u_{n-1})} \\) —— **超曲面法向量的分量表示**。

#### §11.3 链式法则
*   **(11.5)**：\\( Jf(x^0) = \left( \frac{\partial f_i}{\partial x_j} (x^0) \right)_{m \times n} \\) —— **Jacobi 矩阵的定义**。
*   **(11.6)**：\\( Jh(x^0) = Jg(y^0) \cdot Jf(x^0) \\) —— **复合函数求导的链式法则**。
*   **(11.7)**：\\( f(x) - f(x^0) = Jf(x^0)(x - x^0) + o(\|x - x^0\|) \\) —— **向量值函数可微的定义式**。
*   **(11.8)**：\\( g(y) - g(y^0) = Jg(y^0)(y - y^0) + o(\|y - y^0\|) \\) —— **外层函数可微的定义式**。
*   **(11.9)**：\\( \frac{\partial h_i}{\partial x_j}(x^0) = \sum_{k=1}^m \frac{\partial g_i}{\partial y_k}(y^0) \cdot \frac{\partial f_k}{\partial x_j}(x^0) \\) —— **链式法则的分量形式**。
*   **(11.10)**：\\( (f \circ \sigma)'(t^0) = \nabla f(x^0) \cdot \sigma'(t^0) \\) —— **函数沿曲线变化的导数**。
*   **(11.11)**：\\( \nabla f(x) = \sum_{i=1}^n \frac{\partial f}{\partial x_i}(x) e_i \\) —— **梯度场在标准基下的表示**。
*   **(11.12)**：\\( \omega(x) = \sum_{j=1}^n \omega_j(x) e^j \\) —— **1-形式的表示**。
*   **(11.13)**：\\( df = \sum_{j=1}^n \frac{\partial f}{\partial x_j} dx_j \\) —— **全微分的常用表示**。
*   **(11.14)**：\\( dh_i = \sum_{k=1}^m \frac{\partial g_i}{\partial y_k}(f) df_k \\) —— **全微分形式不变性**。

#### §11.4 拟微分中值定理
*   **(11.15)**：\\( f(x) - f(y) = \nabla f(\xi) \cdot (x - y) \\) —— **多元函数微分中值定理**。

#### §11.5 逆映射定理和隐映射定理
*   **(11.16)**：\\( f(x) = y \\) 即 \\( x = y - g(x) \\) —— **逆映射存在的迭代基础方程**。
*   **(11.17)**：\\( \|\varphi(x)\| \le \|y\| + \|g(x)\| < \frac{\delta}{2} + \frac{1}{2} \|x\| \le \delta \\) —— **压缩映射证明中的范围控制**。
*   **(11.18)**：\\( y - g(h(y)) = h(y) \\) —— **逆映射满足的等式**。
*   **(11.19)**：\\( Jh(y) = [Jf(h(y))]^{-1} \\) —— **逆映射的导数公式**。

#### §11.6 多元函数的极值
*   **(11.20)**：\\( f(y) \ge f(x) + \nabla f(x) \cdot (y - x) \\) —— **凸函数的一阶充要条件**。
*   **(11.21)**：\\( \varphi(1) = \varphi(0) + \varphi'(0) + \frac{1}{2!} \varphi''(0) + \dots + \frac{1}{m!} \varphi^{(m)}(0) + R_m \\) —— **一元函数 Taylor 公式应用**。

#### §11.7 Lagrange 乘数法
*   **(11.22)**：\\( \nabla f(x^0) = \sum_{i=1}^m \lambda_i^0 \nabla \varphi_i(x^0) \\) —— **条件极值的必要条件（梯度线性相关）**。
*   **(11.23)**：\\( \nabla f(x^0) - \lambda^0 \cdot J\Phi(x^0) = 0 \\) —— **Lagrange 乘数法的矩阵表示**。
*   **(11.24) - (11.28)**：涉及 \\( J\psi \\) 与 \\( J_y f \\) 的推导，最终得出结论公式。

#### §11.8 补充材料
*   **(11.29)**：\\( \ell(x) = x \cdot w^T = \sum_{i=1}^n x_i w_i \\) —— **线性函数的外积表示**。
*   **(11.30)**：\\( w_i = (-1)^{i-1} \det \begin{pmatrix} v_1^1 & \dots & v_{i-1}^1 & v_{i+1}^1 & \dots & v_n^1 \\ \vdots & & \vdots & \vdots & & \vdots \end{pmatrix} \\) —— **外积向量分量的行列式计算式**。