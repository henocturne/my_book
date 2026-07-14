---
title: "theorem"
weight: 1
bookCollapseSection: true
---
{{< katex display=true >}}
{{< /katex >}}
根据提供的源代码《理论力学基本教程》第七章，书中并未以“定理”或“引理”为标题进行显式标注，而是以**“原理” (Principle)** 或 **“方程” (Equation)** 的形式给出了分析力学的核心规律。在物理学教材中，这些“原理”起到了定理的作用。

以下是按照小节整理的具有定理/引理性质的核心规律：

### §7-1 约束的分类 广义坐标
本节以定义为主，为后续原理提供数学描述基础，未提出具体定理。

### §7-2 虚位移和虚功 理想约束
*   **理想约束条件**：如果作用于力学系统的所有约束力在任意虚位移上的虚功之和为零，即 \\( \sum_{i=1}^n \mathbf{F}_{Ri} \cdot \delta \mathbf{r}_i = 0 \\)，则该约束为理想约束。该条件是后续虚功原理成立的前提。

### §7-3 虚功原理
*   **虚功原理 (Principle of Virtual Work)**：受有理想约束、定常约束的力学系统，保持静止平衡的**必要充分条件**是作用于该系统的全部主动力的虚功之和为零。其数学表达式为：
    \\( \sum_{i=1}^n \mathbf{F}_i \cdot \delta \mathbf{r}_i = 0 \quad \\)
*   **广义平衡方程**：在完整系中，系统平衡的条件是每个广义力都为零，即 \\( Q_\alpha = 0, (\alpha = 1, 2, \dots, s) \\)。
*   **有势系平衡定理**：对于主动力均为保守力的有势系，系统处于静止平衡的充要条件是系统的势能取极值，即 \\( \delta V = 0 \\)。
*   **不定乘子平衡方程**：对于受 \\( k \\) 个完整约束限制的系统，其平衡方程可以表示为包含拉格朗日乘子 \\( \lambda_\mu \\) 的形式：\\( F_{ix} + \sum_{\mu=1}^k \lambda_\mu \frac{\partial f_\mu}{\partial x_i} = 0 \\)（及其 \\( y, z \\) 分量形式）。

### §7-4 哈密顿原理
*   **等时变分运算性质**（类似于引理）：
    1.  变分符号 \\( \delta \\) 与微分符号 \\( d \\) 可以交换运算顺序：\\( \delta(dq) = d(\delta q) \\)。
    2.  变分符号 \\( \delta \\) 与对时间的导数 \\( \frac{d}{dt} \\) 可以交换运算顺序：\\( \delta(\frac{dq}{dt}) = \frac{d}{dt}(\delta q) \\)。
*   **欧拉方程 (Euler Equation)**（变分法的基本定理）：泛函 \\( J = \int_{x_0}^{x_1} F[y(x), y'(x), x] dx \\) 取极值的必要条件是满足方程：
    \\( \frac{\partial F}{\partial y} - \frac{d}{dx} \frac{\partial F}{\partial y'} = 0 \quad \\)
*   **哈密顿原理 (Hamilton's Principle)**：受完整约束的有势系，在位形空间中，真实运动使作用量 \\( S \\) 取极值（通常为极小值，故又称**哈密顿最小作用量原理**）。数学表达式为：
    \\( \delta S = \delta \int_{t_0}^{t_1} L(q_\alpha, \dot{q}_\alpha, t) dt = 0 \quad \\)
*   **一般完整系的哈密顿原理**：对于包含非有势力的系统，原理表述为：
    \\( \int_{t_0}^{t_1} (\delta T + \sum_{\alpha=1}^s Q_\alpha \delta q_\alpha) dt = 0 \quad \\)
    