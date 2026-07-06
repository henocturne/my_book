---
title: "formula"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}

根据源文件《第十三章 多元函数的积分》，按照您的要求对定义和公式进行整理如下：

### 一、 定义整理

*   **定义 12.1.1 (矩形中的 Riemann 积分)**：假设 \\( f: I \rightarrow \mathbb{R} \\) 为矩形 \\( I \\) 中定义的函数。如果存在实数 \\( A \\)，使得任给 \\( \varepsilon > 0 \\)，均存在 \\( \delta > 0 \\)，当分割的模 \\( \|\pi\| < \delta \\) 时，有 \\( |\sum_{i,j} f(\xi_{ij})\sigma(I_{ij}) - A| < \varepsilon, \forall \xi_{ij} \in I_{ij} \\)，则称 \\( f \\) 在 \\( I \\) 中 **Riemann 可积**，记为 \\( A = \iint_I f(x, y) dx dy \\)。
*   **定义 12.1.2 (零测集)**：设 \\( A \subset \mathbb{R}^2 \\) 为平面点集。如果任给 \\( \varepsilon > 0 \\)，存在至多可数个闭矩形 \\( \{I_i\} \\)，使得 \\( A \subset \bigcup_{i \ge 1} I_i \\)，且 \\( \sum_{i \ge 1} \sigma(I_i) < \varepsilon \\)，则称 \\( A \\) 为**零测集**。
*   **定义 12.1.3 (可求面积集)**：设 \\( A \\) 为有界集合，\\( I \\) 为包含 \\( A \\) 的矩形。如果 \\( A \\) 的特征函数 \\( \chi_A \\) 在 \\( I \\) 中可积，则称 \\( A \\) 为**可求面积集**，其面积 \\( \sigma(A) \\) 定义为 \\( \chi_A \\) 在 \\( I \\) 中的积分。
*   **定义 12.1.4 (一般集合上的积分)**：设 \\( A \\) 为可求面积的有界集合，\\( f: A \rightarrow \mathbb{R} \\) 为 \\( A \\) 中定义的有界函数。将 \\( f \\) 零延拓为 \\( f_A \\)。如果 \\( f_A \\) 在包含 \\( A \\) 的矩形 \\( I \\) 中可积，则称 \\( f \\) 在 \\( A \\) 中**可积**，其积分定义为 \\( \int_A f = \int_I f_A \\)。
*   **定义 12.2.1 (\\( n \\) 维矩形中的 Riemann 积分)**：设 \\( f: I \rightarrow \mathbb{R} \\) 为 \\( n \\) 维矩形 \\( I \\) 中定义的函数。如果存在实数 \\( A \\)，使得任给 \\( \varepsilon > 0 \\)，均存在 \\( \delta > 0 \\)，当分割的模 \\( \|\pi\| < \delta \\) 时，有 \\( |\sum_{i_1 \dots i_n} f(\xi_{i_1 \dots i_n})\nu(I_{i_1 \dots i_n}) - A| < \varepsilon \\)，则称 \\( f \\) 在 \\( I \\) 中 **Riemann 可积**。
*   **定义 12.5.1 (穷竭)**：设 \\( \{D_i\} \\) 为 \\( \mathbb{R}^n \\) 中一列可求体积的有界集合，满足：(1) \\( \bar{D_i} \subset int D_{i+1}, \forall i \ge 1 \\)；(2) \\( \bigcup_{i \ge 1} D_i = \mathbb{R}^n \\)，则称 \\( \{D_i\} \\) 为 \\( \mathbb{R}^n \\) 的一个**穷竭**。

---

### 二、 公式整理

*   **(12.1)**：\\( \omega_{2k} = \frac{\pi^k}{k!}, \quad \omega_{2k-1} = \frac{2^k \pi^{k-1}}{(2k-1)!!} \\)
    *   **内容**：给出 \\( 2k \\) 维和 \\( 2k-1 \\) 维单位球体体积 \\( \omega_n \\) 的具体计算数值。
*   **(12.2)**：\\( 2^n n^{-n/2} \le \omega_n \le 2^n \\)
    *   **内容**：\\( n \\) 维单位球体体积 \\( \omega_n \\) 的简单上下界估计。
*   **(12.3)**：\\( \nu(\varphi(A)) = |\det \varphi| \nu(A) \\)
    *   **内容**：描述可求体积集合 \\( A \\) 在**线性变换** \\( \varphi \\) 作用下体积的变化规律。
*   **(12.4)**：\\( \int_{\varphi(A)} f = \int_A f \circ \varphi |\det J\varphi| \\)
    *   **内容**：**重积分的变量替换公式**，将坐标变换下的积分通过 Jacobi 行列式进行转换。
*   **(12.5)**：\\( \int_{A_n} \sin^{n-2} \theta_1 \sin^{n-3} \theta_2 \dots \sin \theta_{n-2} d\theta_1 d\theta_2 \dots d\theta_{n-1} = n \omega_n \\)
    *   **内容**：涉及 \\( n \\) 维球面坐标积分的一个恒等式，常用于计算高维球体体积。
*   **(12.6)**：\\( \omega_n = \frac{2\pi^{n/2}}{n\Gamma(\frac{n}{2})} = \frac{\pi^{n/2}}{\Gamma(\frac{n}{2} + 1)} \\)
    *   **内容**：利用 **Gamma 函数**表示的 \\( n \\) 维单位球体体积的统一公式。