# 洛必达法则失效的振荡函数专题

> 📌 **核心要点**：洛必达法则要求求导后极限存在（或为 $\infty$）。当导数中出现振荡项（如 $\sin\frac{1}{x}$、$\cos x$ 等）且极限不存在时，**洛必达法则失效**。此时需改用等价无穷小、夹逼准则或拆分法。

---

## 类型一：$x \to 0$ 时 $\sin\frac{1}{x}$ 型振荡

### 典例 1：$\displaystyle \lim_{x \to 0} \frac{x^2 \sin\frac{1}{x}}{\sin x}$

**【洛必达 × 失效】** 分子求导：$2x\sin\frac{1}{x} - \cos\frac{1}{x}$，其中 $\cos\frac{1}{x}$ 在 $x\to0$ 时振荡无极限，洛必达不能用。

**正确解法**（等价无穷小）：

$$
\lim_{x\to0} \frac{x^2 \sin\frac{1}{x}}{\sin x}
= \lim_{x\to0} \frac{x^2 \sin\frac{1}{x}}{x}
= \lim_{x\to0} x \sin\frac{1}{x} = 0
$$

> ✅ **答案：$0$**

---

### 典例 2：$\displaystyle \lim_{x \to 0} \frac{x \sin\frac{1}{x}}{\sin x}$

**【洛必达 × 失效】** 分子求导得 $\sin\frac{1}{x} - \frac{1}{x}\cos\frac{1}{x}$，振荡且发散，洛必达失效。

**正确解法**（等价无穷小）：

$$
\lim_{x\to0} \frac{x \sin\frac{1}{x}}{\sin x}
= \lim_{x\to0} \frac{x \sin\frac{1}{x}}{x}
= \lim_{x\to0} \sin\frac{1}{x} \quad\text{不存在}
$$

> ✅ **结论：极限不存在（振荡）**

---

### 典例 3：$\displaystyle \lim_{x \to 0} \frac{x^3 \sin\frac{1}{x}}{x - \sin x}$

**【洛必达 × 失效】** 分子求导出现 $\cos\frac{1}{x}$ 振荡项，洛必达失效。

**正确解法**（等价无穷小 + 泰勒）：

分母 $x - \sin x \sim \frac{x^3}{6}$，分子 $x^3\sin\frac{1}{x}$：

$$
\lim_{x\to0} \frac{x^3 \sin\frac{1}{x}}{x - \sin x}
= \lim_{x\to0} \frac{x^3 \sin\frac{1}{x}}{\frac{x^3}{6}}
= 6 \lim_{x\to0} \sin\frac{1}{x} \quad\text{不存在}
$$

> ✅ **结论：极限不存在（振荡）**

---

## 类型二：$x \to \infty$ 时 $\sin x$、$\cos x$ 型振荡

### 典例 4：$\displaystyle \lim_{x \to \infty} \frac{x + \sin x}{x}$

**【洛必达 × 失效】** 洛必达得 $\displaystyle \lim_{x\to\infty} \frac{1+\cos x}{1}$，$\cos x$ 在无穷远处振荡无极限，洛必达失效。

**正确解法**（拆分法）：

$$
\lim_{x\to\infty} \frac{x + \sin x}{x}
= \lim_{x\to\infty} \left(1 + \frac{\sin x}{x}\right)
= 1 + 0 = 1
$$

> ✅ **答案：$1$**

---

### 典例 5：$\displaystyle \lim_{x \to \infty} \frac{x - \sin x}{x + \sin x}$

**【洛必达 × 失效】** 洛必达后出现 $\frac{1-\cos x}{1+\cos x}$，$\cos x$ 振荡，极限不存在，洛必达失效。

**正确解法**（同除 $x$）：

$$
\lim_{x\to\infty} \frac{x - \sin x}{x + \sin x}
= \lim_{x\to\infty} \frac{1 - \frac{\sin x}{x}}{1 + \frac{\sin x}{x}}
= \frac{1 - 0}{1 + 0} = 1
$$

> ✅ **答案：$1$**

---

### 典例 6：$\displaystyle \lim_{x \to \infty} \frac{x + \sin x}{x - \cos x}$

**【洛必达 × 失效】** 求导后出现 $\frac{1+\cos x}{1+\sin x}$，分子分母均振荡，极限不存在，洛必达失效。

**正确解法**（同除 $x$）：

$$
\lim_{x\to\infty} \frac{x + \sin x}{x - \cos x}
= \lim_{x\to\infty} \frac{1 + \frac{\sin x}{x}}{1 - \frac{\cos x}{x}}
= \frac{1 + 0}{1 - 0} = 1
$$

> ✅ **答案：$1$**

---

## 类型三：$x \to \infty$ 时 $\sin x^2$、$x\sin x$ 等混合振荡

### 典例 7：$\displaystyle \lim_{x \to \infty} \frac{x^2 + \sin x}{x^2 + \cos x}$

**【洛必达 × 失效】** 求导得 $\frac{2x + \cos x}{2x - \sin x}$，再次求导得 $\frac{2 - \sin x}{2 - \cos x}$，分子分母均振荡，洛必达彻底失效。

**正确解法**（同除 $x^2$）：

$$
\lim_{x\to\infty} \frac{1 + \frac{\sin x}{x^2}}{1 + \frac{\cos x}{x^2}}
= \frac{1 + 0}{1 + 0} = 1
$$

> ✅ **答案：$1$**

---

## 💡 洛必达失效判定与应对策略

| 情形 | 特征 | 失效原因 | 应对策略 |
|:---|:---|:---|:---|
| **$x \to 0$，含 $\sin\frac{1}{x}$** | 分子/分母出现 $\sin\frac{1}{x}$、$\cos\frac{1}{x}$ | 求导后 $\cos\frac{1}{x}$ 振荡无极限 | 等价无穷小代换，消去振荡因子 |
| **$x \to \infty$，含 $\sin x$** | 分子/分母含 $\sin x$、$\cos x$ | 求导后 $\sin x$、$\cos x$ 振荡无极限 | 同除最高次幂，夹逼准则 |
| **可导但导数振荡** | $f(x)=x^2\sin\frac{1}{x}$ 类函数 | $f'(x)$ 在 $x=0$ 附近无极限 | 用定义或等价替换 |
| **分子分母均振荡** | 如 $\frac{1+\cos x}{1+\sin x}$ | 分子分母同时振荡，极限不存在 | 拆分或同除最高次 |

> **记忆口诀**：见到 $\sin\frac{1}{x}$ 洛必达先别急，等价代换是第一；见到 $\sin x$ 跑无穷，同除最高最轻松。

---

> 📎 **关联文件**：[泰勒展开与等价无穷小](Math/calculus_taylor.md) | [极限例题精讲](Math/calculus_limit.md) | [返回考研总览](../)
