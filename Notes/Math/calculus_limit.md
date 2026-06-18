# 极限例题精讲

> 📌 **本章内容**：无穷小比阶、$0/0$ 型极限、$1^\infty$ 型极限、数列极限、无穷大 × 周期函数、复合函数反推内层极限

---

## 一、无穷小比阶

### 例题：无穷小比阶 + 泰勒展开

> **题目**：设 $\cos x - 1 = x \sin \alpha(x)$，其中 $|\alpha(x)| < \frac{\pi}{2}$，则当 $x \to 0$ 时，$\alpha(x)$ 是 $x$ 的（ ）
>
> A. 高阶无穷小　B. 低阶无穷小　C. 同阶但不等价无穷小　D. 等价无穷小

**思路分析**：

本题考察**无穷小比阶**，核心是求 $\displaystyle\lim_{x\to0}\frac{\alpha(x)}{x}$。题目给出了 $\cos x - 1 = x\sin\alpha(x)$ 这一桥梁条件，可以通过等价无穷小 $\alpha \sim \sin\alpha$ 将 $\alpha(x)$ 与已知条件连接起来，再用泰勒展开 $\cos x$ 到二阶即可。

---

**解法一：比值法（老师讲法·目标导向）**

要判断 $\alpha(x)$ 是 $x$ 的什么无穷小，直接求比值的极限：

$$
\lim_{x\to0}\frac{\alpha(x)}{x}
$$

由于 $x\to0$ 时 $\alpha(x)\to0$（由 $|\alpha(x)|<\frac{\pi}{2}$ 及等式可推），利用等价无穷小 $\alpha \sim \sin\alpha$：

$$
\frac{\alpha(x)}{x} \sim \frac{\sin\alpha(x)}{x}
$$

上下同乘 $x$，凑出题目条件中的 $x\sin\alpha(x)$：

$$
\frac{\sin\alpha(x)}{x} = \frac{x\sin\alpha(x)}{x^2}
$$

代入已知等式 $\cos x - 1 = x\sin\alpha(x)$：

$$
\frac{\alpha(x)}{x} \sim \frac{\cos x - 1}{x^2}
$$

对 $\cos x$ 泰勒展开：$\cos x = 1 - \dfrac{x^2}{2} + O(x^4)$

$$
\cos x - 1 = -\frac{x^2}{2} + O(x^4)
$$

$$
\lim_{x\to0}\frac{\alpha(x)}{x} = \lim_{x\to0}\frac{-\frac{x^2}{2}}{x^2} = -\frac{1}{2}
$$

极限存在且为非零常数 $-\frac{1}{2}$，所以 $\alpha(x)$ 与 $x$ **同阶但不等价**。

> ✅ **答案：C**

---

**解法二：等式法（直接解出 $\alpha(x)$ 的表达式）**

对已知等式 $\cos x - 1 = x\sin\alpha(x)$，泰勒展开左端：

$$
\cos x - 1 = -\frac{x^2}{2} + O(x^4)
$$

代入：

$$
-\frac{x^2}{2} + O(x^4) = x\sin\alpha(x)
$$

两边同除以 $x$：

$$
\sin\alpha(x) = -\frac{x}{2} + O(x^3)
$$

当 $x\to0$ 时 $\sin\alpha(x)\to0$，结合 $|\alpha(x)|<\frac{\pi}{2}$ 知 $\alpha(x)\to0$，由 $\sin\alpha\sim\alpha$：

$$
\alpha(x) \sim -\frac{x}{2}
$$

同阶不等价，系数 $-\frac{1}{2}$。

> ✅ **答案：C**

---

> 💡 **启示**：
> - **解法一**更直接：判断 $\alpha(x)$ 与 $x$ 的阶 → 直接求 $\alpha(x)/x$ → 凑已知条件 → 泰勒展开一步到位
> - **解法二**更直观：从等式解出 $\alpha(x)$ 的渐近表达式再判断，适合对等价替换不熟练时使用
> - 关键桥梁：$\alpha \sim \sin\alpha$（$\alpha\to0$），这是连接 $\alpha(x)$ 和 $\sin\alpha(x)$ 的纽带

---

## 二、$0/0$ 型极限

### 例题：$0/0$ 型极限 · 三步法

> **题目**：求极限 $\displaystyle \lim_{x \to 0} \frac{\tan x - \sin x}{x^3}$

**解法一：等价无穷小**

直接代换 $\tan x \sim x$，$\sin x \sim x$ 会得到 $\frac{0}{0}$，说明精度不够，需要展开到更高阶。

**解法二：泰勒展开**

$$
\tan x = x + \frac{x^3}{3} + O(x^5)
$$

$$
\sin x = x - \frac{x^3}{6} + O(x^5)
$$

$$
\tan x - \sin x = \left(x + \frac{x^3}{3}\right) - \left(x - \frac{x^3}{6}\right) + O(x^5) = \frac{x^3}{2} + O(x^5)
$$

$$
\lim_{x \to 0} \frac{\tan x - \sin x}{x^3} = \lim_{x \to 0} \frac{\frac{x^3}{2}}{x^3} = \frac{1}{2}
$$

**解法三：提取公因式 + 等价代换**

$$
\tan x - \sin x = \sin x\left(\frac{1}{\cos x} - 1\right) = \sin x \cdot \frac{1-\cos x}{\cos x}
$$

当 $x \to 0$：$\sin x \sim x$，$1-\cos x \sim \frac{x^2}{2}$，$\cos x \to 1$

$$
\lim_{x \to 0} \frac{x \cdot \frac{x^2}{2}}{x^3} = \frac{1}{2}
$$

> ✅ **答案：$\dfrac{1}{2}$**

> 💡 **启示**：等价无穷小替换加减法时要小心！$\tan x - \sin x$ 不能直接用 $x-x=0$，因为两项抵消后高阶项成为主导，必须展开到足够阶数。

---

### 例题：$0/0$ 型极限 · 泰勒展开 / 洛必达

> **题目**：设 $f(x)$ 二阶可导，$f(0)=0$，$f'(0)=1$，$f''(0)=2$，求极限 $\displaystyle\lim_{x\to 0}\frac{f(x)}{x^2}$。

**思路分析**：已知函数在 $x=0$ 处的函数值、一阶和二阶导数值，考虑用**泰勒展开**将 $f(x)$ 展开到 $x^2$ 项，或使用**洛必达法则**逐步求导。由于 $f(0)=0$，$f'(0)=1\neq 0$，$f(x)$ 在 $x=0$ 附近的一次项主导，分母为 $x^2$，极限应为 $\infty$。

---

**解法一（泰勒展开法）**：

由 $f(x)$ 二阶可导，在 $x=0$ 处泰勒展开到 $x^2$ 项：

$$
f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + o(x^2)
= 0 + 1\cdot x + \frac{2}{2}x^2 + o(x^2)
= x + x^2 + o(x^2)
$$

代入极限：

$$
\lim_{x\to 0} \frac{f(x)}{x^2}
= \lim_{x\to 0} \frac{x + x^2 + o(x^2)}{x^2}
= \lim_{x\to 0} \left(\frac{1}{x} + 1 + \frac{o(x^2)}{x^2}\right)
= \infty
$$

---

**解法二（洛必达法则）**：

$$
\lim_{x\to 0} \frac{f(x)}{x^2}
\xrightarrow{\frac{0}{0}}
\lim_{x\to 0} \frac{f'(x)}{2x}
$$

由于 $f'(0)=1 \neq 0$，分子 $\to 1$，分母 $\to 0$，故

$$
\lim_{x\to 0} \frac{f'(x)}{2x} = \infty
$$

---

> **答案**：$\boxed{\infty}$

💡 **启示与要点**：
1. 本题关键是识别 $f(x) \sim x$（一次项主导），分母为 $x^2$，因此极限为 $\infty$，属于**无穷大**情形。
2. 若将分母改为 $x$，则 $\displaystyle\lim_{x\to0}\frac{f(x)}{x}=f'(0)=1$，这是导数定义的直接应用。
3. 若将分子改为 $f(x)-x$，则 $\displaystyle\lim_{x\to0}\frac{f(x)-x}{x^2}=\frac{f''(0)}{2}=1$，体现了二阶导数在极限中的作用。

---

### 例题：$0/0$ 型极限 · 三角复合·洛必达 + 泰勒

> **题目**：求极限 $\displaystyle \lim_{x \to 1} \frac{\ln \cos(x-1)}{1 - \sin\left(\frac{\pi}{2}x\right)}$

**思路分析**：

$x \to 1$ 时分子分母均 $\to 0$，为 **$0/0$ 型未定式**。

关键观察：分母 $\sin\left(\frac{\pi}{2}x\right)$ 在 $x=1$ 处可凑成余弦形式。令 $t = x-1$ 换元，将 $x\to1$ 转化为 $t\to0$，便于使用常见等价无穷小和泰勒展开。

---

**换元**：令 $t = x-1$，则 $x = t+1$，$t \to 0$。

分母处理（核心技巧）：

$$
\sin\left(\frac{\pi}{2}x\right) = \sin\left(\frac{\pi}{2}(t+1)\right) = \sin\left(\frac{\pi}{2}t + \frac{\pi}{2}\right) = \cos\left(\frac{\pi}{2}t\right)
$$

原式化为：

$$
\lim_{t \to 0} \frac{\ln \cos t}{1 - \cos\left(\frac{\pi}{2}t\right)}
$$

---

**解法一：泰勒展开（等价无穷小）**

当 $t \to 0$ 时：

- $\cos t = 1 - \dfrac{t^2}{2} + O(t^4)$
- $\ln \cos t = \ln\!\left(1 - \dfrac{t^2}{2} + O(t^4)\right) \sim -\dfrac{t^2}{2}$
- $\cos\left(\dfrac{\pi}{2}t\right) = 1 - \dfrac{1}{2}\left(\dfrac{\pi}{2}t\right)^2 + O(t^4) = 1 - \dfrac{\pi^2 t^2}{8} + O(t^4)$
- $1 - \cos\left(\dfrac{\pi}{2}t\right) \sim \dfrac{\pi^2 t^2}{8}$

代入原式：

$$
\lim_{t \to 0} \frac{-\dfrac{t^2}{2}}{\dfrac{\pi^2 t^2}{8}} = -\frac{1}{2} \times \frac{8}{\pi^2} = -\frac{4}{\pi^2}
$$

> ✅ **答案：$-\dfrac{4}{\pi^2}$**

---

**解法二：洛必达法则**

对 $\displaystyle \lim_{t \to 0} \frac{\ln \cos t}{1 - \cos\left(\frac{\pi}{2}t\right)}$ 用洛必达：

分子求导：$\dfrac{d}{dt}\ln\cos t = \dfrac{-\sin t}{\cos t} = -\tan t$

分母求导：$\dfrac{d}{dt}\!\left[1 - \cos\left(\dfrac{\pi}{2}t\right)\right] = \dfrac{\pi}{2}\sin\left(\dfrac{\pi}{2}t\right)$

$$
\lim_{t \to 0} \frac{-\tan t}{\dfrac{\pi}{2}\sin\left(\dfrac{\pi}{2}t\right)}
$$

当 $t \to 0$：$\tan t \sim t$，$\sin\left(\dfrac{\pi}{2}t\right) \sim \dfrac{\pi}{2}t$

$$
\lim_{t \to 0} \frac{-t}{\dfrac{\pi}{2} \cdot \dfrac{\pi}{2}t} = \frac{-1}{\dfrac{\pi^2}{4}} = -\frac{4}{\pi^2}
$$

> ✅ **答案：$-\dfrac{4}{\pi^2}$**

---

> 💡 **启示**：
> - **换元 $t = x-1$** 是此类 $x\to1$ 极限的标准操作，把非 $0$ 点极限化为 $0$ 点极限
> - **分母处理**：$\sin(\frac{\pi}{2}x) \xrightarrow{x=t+1} \cos(\frac{\pi}{2}t)$，利用的是 $\sin(\theta+\frac{\pi}{2}) = \cos\theta$ 的诱导公式
> - 转化后的问题 $\displaystyle\lim_{t\to0}\frac{\ln\cos t}{1-\cos(at)}$ 形态非常规整，两种方法皆可
> - 注意洛必达后分子 $\tan t \sim t$、分母 $\sin(\frac{\pi}{2}t) \sim \frac{\pi}{2}t$，比例系数刚好消去 $t$，得到常数

---

## 三、$1^\infty$ 型极限

### 例题：$1^\infty$ 型极限 · 重要极限法

> **题目**：求极限 $\displaystyle \lim_{x \to 0} (\cos x)^{\frac{1}{x^2}}$

**解法**：

这是 $1^\infty$ 型未定式。取对数：

$$
\text{令 } y = (\cos x)^{\frac{1}{x^2}}, \quad \ln y = \frac{\ln(\cos x)}{x^2}
$$

由泰勒展开：$\cos x = 1 - \frac{x^2}{2} + O(x^4)$

$$
\ln(\cos x) = \ln\left(1 - \frac{x^2}{2} + O(x^4)\right)
$$

当 $u \to 0$ 时，$\ln(1+u) \sim u$，所以：

$$
\ln(\cos x) \sim -\frac{x^2}{2}
$$

$$
\lim_{x \to 0} \ln y = \lim_{x \to 0} \frac{-\frac{x^2}{2}}{x^2} = -\frac{1}{2}
$$

$$
\lim_{x \to 0} y = e^{-1/2} = \frac{1}{\sqrt{e}}
$$

> ✅ **答案：$e^{-1/2}$**

---

### 例题：$1^\infty$ 型极限 · 公式法速解（2022 数二/数三真题）

> **题目**（例18·2022 数二、数三）：求极限 $\displaystyle \lim_{x \to 0} \left(\frac{1+e^{x}}{2}\right)^{\cot x} = \underline{\qquad}$

**思路分析**：

$x \to 0$ 时，$\frac{1+e^{x}}{2} \to \frac{1+1}{2}=1$，$\cot x \to \infty$，为 **$1^\infty$ 型未定式**。

$1^\infty$ 型有快速公式：$\lim u^v = e^{\lim v(u-1)}$（前提 $\lim u = 1, \lim v = \infty$）。

---

**解法一：$1^\infty$ 公式法（最快）**

令 $u = \dfrac{1+e^{x}}{2}$，$v = \cot x$。

**第一步**：求 $u-1$

$$
u - 1 = \frac{1+e^{x}}{2} - 1 = \frac{e^{x} - 1}{2}
$$

当 $x \to 0$ 时，$e^{x} - 1 \sim x$，所以：

$$
u - 1 \sim \frac{x}{2}
$$

**第二步**：求 $v(u-1)$

$$
v(u-1) = \cot x \cdot (u-1) \sim \frac{\cos x}{\sin x} \cdot \frac{x}{2}
$$

当 $x \to 0$：$\sin x \sim x$，$\cos x \to 1$：

$$
v(u-1) \sim \frac{1}{x} \cdot \frac{x}{2} = \frac{1}{2}
$$

**第三步**：代入公式

$$
\lim_{x \to 0} \left(\frac{1+e^{x}}{2}\right)^{\cot x} = e^{\lim v(u-1)} = e^{1/2}
$$

> ✅ **答案：$e^{1/2}$**

---

**解法二：取对数 + 泰勒展开（通用法）**

令 $y = \left(\dfrac{1+e^{x}}{2}\right)^{\cot x}$，取对数：

$$
\ln y = \cot x \cdot \ln\left(\frac{1+e^{x}}{2}\right) = \frac{\cos x}{\sin x} \cdot \ln\left(\frac{1+e^{x}}{2}\right)
$$

$x \to 0$ 时，$\sin x \sim x$，$\cos x \to 1$：

$$
\ln y \sim \frac{1}{x} \cdot \ln\left(\frac{1+e^{x}}{2}\right)
$$

对 $e^{x}$ 泰勒展开：$e^{x} = 1 + x + \dfrac{x^2}{2} + \dfrac{x^3}{6} + O(x^4)$

$$
\frac{1+e^{x}}{2} = 1 + \frac{x}{2} + \frac{x^2}{4} + \frac{x^3}{12} + O(x^4)
$$

令 $t = \dfrac{x}{2} + \dfrac{x^2}{4} + \dfrac{x^3}{12}$，则 $\ln(1+t) = t - \dfrac{t^2}{2} + O(t^3)$：

$$
\begin{aligned}
\ln\left(\frac{1+e^{x}}{2}\right) &= \left(\frac{x}{2} + \frac{x^2}{4} + \frac{x^3}{12}\right) - \frac{1}{2}\left(\frac{x}{2} + \frac{x^2}{4}\right)^2 + O(x^3) \\
&= \frac{x}{2} + \frac{x^2}{4} + \frac{x^3}{12} - \frac{1}{2}\left(\frac{x^2}{4} + \frac{x^3}{4}\right) + O(x^3) \\
&= \frac{x}{2} + \frac{x^2}{8} + O(x^3)
\end{aligned}
$$

$$
\ln y \sim \frac{1}{x}\left(\frac{x}{2} + \frac{x^2}{8}\right) = \frac{1}{2} + \frac{x}{8} \to \frac{1}{2}
$$

$$
\lim y = e^{1/2}
$$

> ✅ **答案：$e^{1/2}$**

---

> 💡 **启示**：
> - **$1^\infty$ 型首选公式**：$\lim u^v = e^{\lim v(u-1)}$，三步出答案
> - 本题 $u-1 \sim \frac{x}{2}$，$v \sim \frac{1}{x}$，相乘即得 $\frac{1}{2}$
> - 取对数法虽然慢但通用，当 $u-1$ 不便泰勒展开时用
> - 与例题5对比：都是 $1^\infty$ 型，但本题用公式法更快

---

### 例题：$1^\infty$ 型极限 · 数列极限·几何平均（经典题）

> **题目**（20）：求极限 $\displaystyle \lim_{n \to \infty} \left(\frac{\sqrt[n]{a} + \sqrt[n]{b} + \sqrt[n]{c}}{3}\right)^n$，其中 $a > 0$，$b > 0$，$c > 0$。

**思路分析**：

$n \to \infty$ 时，$\sqrt[n]{a} = a^{1/n} \to 1$，底数 $\to \frac{1+1+1}{3}=1$，指数 $n \to \infty$，为 **$1^\infty$ 型**。

关键技巧：$a^{1/n} = e^{\frac{\ln a}{n}}$，利用 $e^x - 1 \sim x$ 展开到一阶即可。

---

**解法一：$1^\infty$ 公式法**

令 $u = \dfrac{a^{1/n} + b^{1/n} + c^{1/n}}{3}$，$v = n$。

展开 $a^{1/n} = e^{\frac{\ln a}{n}} = 1 + \dfrac{\ln a}{n} + O\!\left(\dfrac{1}{n^2}\right)$

同理 $b^{1/n} = 1 + \dfrac{\ln b}{n} + O\!\left(\dfrac{1}{n^2}\right)$，$c^{1/n} = 1 + \dfrac{\ln c}{n} + O\!\left(\dfrac{1}{n^2}\right)$

$$
u = \frac{3 + \frac{\ln a + \ln b + \ln c}{n} + O(\frac{1}{n^2})}{3}
= 1 + \frac{\ln(abc)}{3n} + O\!\left(\frac{1}{n^2}\right)
$$

$$
u - 1 \sim \frac{\ln(abc)}{3n}
$$

$$
v(u-1) = n \cdot \frac{\ln(abc)}{3n} = \frac{\ln(abc)}{3}
$$

$$
\lim_{n \to \infty} u^v = e^{\lim v(u-1)} = e^{\frac{\ln(abc)}{3}} = (abc)^{1/3} = \sqrt[3]{abc}
$$

> ✅ **答案：$\sqrt[3]{abc}$**

---

**解法二：取对数法**

令 $y_n = \left(\dfrac{a^{1/n} + b^{1/n} + c^{1/n}}{3}\right)^n$

$$
\ln y_n = n \ln\!\left(\frac{a^{1/n} + b^{1/n} + c^{1/n}}{3}\right)
$$

令 $t = \dfrac{1}{n} \to 0^+$，则：

$$
\ln y_n = \frac{1}{t} \ln\!\left(\frac{a^t + b^t + c^t}{3}\right)
$$

转化为函数极限（$t \to 0^+$ 的 $\frac{0}{0}$ 型），用洛必达：

$$
\lim_{t \to 0} \frac{\ln(a^t + b^t + c^t) - \ln 3}{t}
= \lim_{t \to 0} \frac{a^t \ln a + b^t \ln b + c^t \ln c}{a^t + b^t + c^t}
$$

> ⚠️ **关键一步**：此时分子分母各部分的极限**均存在**，可以拆开分别计算：
>
> - 分子：$\lim a^t \ln a = \ln a$，$\lim b^t \ln b = \ln b$，$\lim c^t \ln c = \ln c$
> - 分母：$\lim (a^t + b^t + c^t) = 3 \neq 0$
>
> 因此可将极限"穿透"到分子分母内部：

$$
= \frac{\ln a + \ln b + \ln c}{3} = \frac{\ln(abc)}{3}
$$

$$
\lim y_n = e^{\frac{\ln(abc)}{3}} = \sqrt[3]{abc}
$$

> ✅ **答案：$\sqrt[3]{abc}$**

---

> 💡 **启示**：
> - 结果 $\sqrt[3]{abc}$ 恰好是 $a,b,c$ 的**几何平均数**——这是本题最漂亮的结论
> - 推广：$\displaystyle \lim_{n\to\infty}\!\left(\frac{\sqrt[n]{a_1}+\cdots+\sqrt[n]{a_k}}{k}\right)^n = \sqrt[k]{a_1 a_2 \cdots a_k}$
> - 关键展开：$a^{1/n} = 1 + \frac{\ln a}{n} + o(\frac{1}{n})$，只须一阶
> - 洛必达法也很自然：$n\to\infty$ 换元 $t=1/n$，化数列极限为函数极限
> - **拆项技巧**：洛必达后分子分母各部分极限均存在且分母 $\neq 0$，可直接将极限分配到各项

---

## 四、数列极限

### 例题：数列极限 · 定积分定义

> **题目**：求极限 $\displaystyle \lim_{n \to \infty} \sum_{k=1}^{n} \frac{n}{n^2 + k^2}$

**解法**：

将和式改写为定积分定义的形式：

$$
\sum_{k=1}^{n} \frac{n}{n^2 + k^2} = \frac{1}{n} \sum_{k=1}^{n} \frac{1}{1 + \left(\frac{k}{n}\right)^2}
$$

令 $x_k = \frac{k}{n}$，$\Delta x = \frac{1}{n}$，则：

$$
\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \frac{1}{1 + \left(\frac{k}{n}\right)^2} = \int_0^1 \frac{1}{1+x^2}\,dx = \arctan x \Big|_0^1 = \frac{\pi}{4}
$$

> ✅ **答案：$\dfrac{\pi}{4}$**

> 💡 **要点**：看到 $\frac{1}{n}\sum f(\frac{k}{n})$ 形式 → 定积分定义 $\int_0^1 f(x)dx$

---

### 例题：数列极限 · 定积分定义（调和型）

> **题目**：$\displaystyle \lim_{n \to \infty}\left(\frac{1}{n+1}+\frac{1}{n+2}+\cdots+\frac{1}{n+n}\right)=\underline{\quad}$

**思路分析**：

这是典型的**定积分定义求和极限**问题。和式中的每一项为 $\frac{1}{n+k}$（$k=1,\dots,n$），分母 $n+k$ 随 $k$ 变化。核心思路是提出因子 $\frac{1}{n}$，将和式化为 $\frac{1}{n}\sum f(\frac{k}{n})$ 的标准形式。

---

**解法一：定积分定义**

$$
\lim_{n \to \infty} \sum_{k=1}^{n} \frac{1}{n+k}
= \lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \frac{1}{1+\frac{k}{n}}
$$

令 $x_k = \frac{k}{n}$，$\Delta x = \frac{1}{n}$，则上式化为定积分：

$$
\lim_{n \to \infty} \frac{1}{n} \sum_{k=1}^{n} \frac{1}{1+\frac{k}{n}}
= \int_0^1 \frac{1}{1+x}\,dx
= \ln(1+x)\Big|_0^1
= \ln 2
$$

---

**解法二：调和级数近似（欧拉常数）**

令 $H_n = 1 + \frac{1}{2} + \cdots + \frac{1}{n}$（第 $n$ 个调和数），则：

$$
\sum_{k=1}^{n} \frac{1}{n+k} = H_{2n} - H_n
$$

由欧拉-麦克劳林公式，$H_n = \ln n + \gamma + o(1)$（$\gamma$ 为欧拉常数），故：

$$
H_{2n} - H_n = (\ln 2n + \gamma) - (\ln n + \gamma) + o(1) = \ln 2 + o(1)
$$

$$
\lim_{n \to \infty} (H_{2n} - H_n) = \ln 2
$$

---

> ✅ **答案**：$\boxed{\ln 2}$

💡 **启示与对比**：
1. 与**上一题**对比：两者都是 $\frac{1}{n}\sum f(\frac{k}{n})$ 形式的定积分定义问题，但上一题的被积函数为 $\frac{1}{1+x^2}$，本题为 $\frac{1}{1+x}$，结果分别为 $\frac{\pi}{4}$ 和 $\ln 2$。
2. **关键变形**：$\frac{1}{n+k} = \frac{1}{n}\cdot\frac{1}{1+\frac{k}{n}}$，将分母中的 $n+k$ 拆出 $n$ 因子是定积分定义的标准手法。
3. 解法二利用调和级数近似，提供了一个更宏观的视角——此类求和可看作 $\ln$ 函数的离散化。

---

### 例题：数列收敛的 ε-N 定义辨析

> **题目**（例13·1999 数二）："对任意给定的 $\varepsilon \in (0,1)$，总存在正整数 $N$，当 $n \geq N$ 时，恒有 $|x_n - a| \leq 2\varepsilon$" 是数列 $\{x_n\}$ 收敛于 $a$ 的（ ）
>
> A. 充分条件但非必要条件
> B. 必要条件但非充分条件
> C. 充分必要条件
> D. 既非充分也非必要条件

**思路分析**：

此题考察对**数列极限 ε-N 定义**的精确理解。标准定义为：

$$
\forall \varepsilon > 0,\ \exists N \in \mathbb{N}^+,\ \text{当}\ n \geq N\ \text{时},\ |x_n - a| < \varepsilon
$$

题目条件与之有两处不同：
1. $\varepsilon$ 范围从 $(0, +\infty)$ 缩小到 $(0, 1)$
2. 不等式从 $< \varepsilon$ 变为 $\leq 2\varepsilon$

需分别验证**充分性**（题目条件 ⇒ 收敛）和**必要性**（收敛 ⇒ 题目条件）。

---

**解法一：正反两面推导**

**第一步：必要性（收敛 ⇒ 题目条件）** ← 较简单

设 $\{x_n\}$ 收敛于 $a$，则对任意 $\varepsilon_0 > 0$，存在 $N$，$n \geq N$ 时 $|x_n - a| < \varepsilon_0$。

今对任意给定的 $\varepsilon \in (0,1)$，取 $\varepsilon_0 = \varepsilon$，则存在 $N$ 使：

$$
|x_n - a| < \varepsilon
$$

由于 $\varepsilon > 0$，显然 $\varepsilon < 2\varepsilon$，因此：

$$
|x_n - a| < \varepsilon < 2\varepsilon \quad\Rightarrow\quad |x_n - a| \leq 2\varepsilon
$$

必要性成立 ✅

---

**第二步：充分性（题目条件 ⇒ 收敛）** ← 关键

已知：$\forall \varepsilon \in (0,1), \exists N, n \geq N \Rightarrow |x_n - a| \leq 2\varepsilon$

要证：$\forall \varepsilon_0 > 0, \exists N, n \geq N \Rightarrow |x_n - a| < \varepsilon_0$

对任意 $\varepsilon_0 > 0$，分两种情况：

**情况一**：$\varepsilon_0 \geq 2$

取 $\varepsilon = \dfrac{1}{2} \in (0,1)$，由已知条件，存在 $N$ 使：

$$
|x_n - a| \leq 2 \times \frac{1}{2} = 1 < 2 \leq \varepsilon_0
$$

**情况二**：$\varepsilon_0 < 2$

取 $\varepsilon = \dfrac{\varepsilon_0}{3}$。因 $\varepsilon_0 < 2$，故 $\dfrac{\varepsilon_0}{3} < \dfrac{2}{3} < 1$，即 $\varepsilon \in (0,1)$。

由已知条件，存在 $N$ 使：

$$
|x_n - a| \leq 2\varepsilon = 2 \times \frac{\varepsilon_0}{3} = \frac{2\varepsilon_0}{3} < \varepsilon_0
$$

两种情况均能找到 $N$ 满足 $|x_n - a| < \varepsilon_0$，充分性成立 ✅

---

**结论**：题目条件既是充分的也是必要的 → **充分必要条件**

> ✅ **答案：C**

---

**解法二：等价性理解（快速判断）**

两个"放宽"实际上不影响等价性：

| 差异 | 分析 |
|:---|:---|
| $\varepsilon\in(0,1)$ | 极限只关心 $\varepsilon$ 可以任意小，$(0,1)$ 已经覆盖了"任意小"的范围，大 $\varepsilon$ 自动成立 |
| $\leq 2\varepsilon$ | 因为 $\varepsilon$ 是任意的，$2\varepsilon$ 也是任意的，"$\leq 2\varepsilon$"与"$<\varepsilon$"本质上等价（令 $\varepsilon' = \varepsilon/2$ 即可互换） |

因此该条件与标准 ε-N 定义**等价**。

> ✅ **答案：C**

---

> 💡 **启示**：
> - ε-N 定义的核心是"$\varepsilon$ 可以**任意小**"，只要覆盖了 $(0, \delta)$ 区间即可
> - 不等号是 $<$ 还是 $\leq$、系数是 $1$ 还是 $2$ 还是 $M$，都不影响等价性——因为这些都可以通过缩放 $\varepsilon$ 来消除
> - 考研常考这种"变形定义是否等价"的辨析题，抓住**任意小**这个本质

---

### 例题：数列极限 · 单调有界准则（递推数列）

> **题目**：设 $x_1 > 0$，$x_{n+1} = \dfrac{1}{2}\left(x_n + \dfrac{1}{x_n}\right)$（$n = 1, 2, \dots$），求极限 $\displaystyle\lim_{n \to \infty} x_n$。

**思路分析**：

这是典型的**递推数列求极限**问题，核心方法是**单调有界准则**：先证数列单调且有界，再对递推式两边取极限求值。也可通过代数变形直接得到收敛速度。

---

**解法一：单调有界准则**

**第一步：有界性**

由 $x_1 > 0$ 及递推式显然 $x_n > 0$（$\forall n$）。对 $n \ge 1$，由 AM–GM 不等式：

$$
x_{n+1} = \frac{1}{2}\left(x_n + \frac{1}{x_n}\right) \ge \sqrt{x_n \cdot \frac{1}{x_n}} = 1
$$

故 $x_n \ge 1$（$n \ge 2$），数列有下界 $1$。

**第二步：单调性**

$$
x_{n+1} - x_n = \frac{1}{2}\left(x_n + \frac{1}{x_n}\right) - x_n
= \frac{1}{2}\left(\frac{1}{x_n} - x_n\right)
= \frac{1 - x_n^2}{2x_n}
$$

当 $n \ge 2$ 时 $x_n \ge 1$，故 $1 - x_n^2 \le 0$，即 $x_{n+1} - x_n \le 0$。因此 $\{x_n\}_{n\ge 2}$ 单调递减。

**第三步：求极限**

$\{x_n\}$ 单调递减有下界 ⇒ 极限存在。设 $\displaystyle\lim_{n\to\infty} x_n = a$（$a \ge 1$）。

对递推式两边取极限：

$$
a = \frac{1}{2}\left(a + \frac{1}{a}\right)
\;\Longrightarrow\; 2a = a + \frac{1}{a}
\;\Longrightarrow\; a = \frac{1}{a}
\;\Longrightarrow\; a^2 = 1
$$

由 $a \ge 1$ 得 $a = 1$。

> ✅ **答案：$1$**

---

**解法二：代数变形（平方收敛）**

$$
x_{n+1} - 1 = \frac{1}{2}\left(x_n + \frac{1}{x_n}\right) - 1
= \frac{x_n^2 + 1 - 2x_n}{2x_n}
= \frac{(x_n - 1)^2}{2x_n}
$$

若 $x_1 = 1$，则 $x_n \equiv 1$，极限为 $1$。

若 $x_1 \neq 1$，由上式知 $x_{n+1} - 1$ 与 $(x_n - 1)^2$ 同阶，即**平方收敛**到 $0$，故 $\displaystyle\lim_{n\to\infty} x_n = 1$。

> ✅ **答案：$\boxed{1}$**

---

**解法三：数学归纳法（单调有界）**

核心思路：用数学归纳法一次性证明 $\{x_n\}_{n\ge 2}$ **单调递减且有下界 $1$**。

**第一步：归纳假设**

设命题 $P(n)$：$1 \le x_{n+1} \le x_n$（$n \ge 2$），即从第 $2$ 项起数列单调递减且以 $1$ 为下界。

**第二步：验证基础步 $P(2)$**

先算 $x_2$：

$$
x_2 = \frac{1}{2}\left(x_1 + \frac{1}{x_1}\right)
$$

由 AM–GM 不等式：

$$
x_2 \ge \sqrt{x_1 \cdot \frac{1}{x_1}} = 1
$$

再算 $x_3$，同理：

$$
x_3 = \frac{1}{2}\left(x_2 + \frac{1}{x_2}\right) \ge 1
$$

接着比较 $x_3$ 与 $x_2$：

$$
x_3 - x_2 = \frac{1}{2}\left(x_2 + \frac{1}{x_2}\right) - x_2
= \frac{1}{2}\left(\frac{1}{x_2} - x_2\right)
= \frac{1 - x_2^2}{2x_2} \le 0
$$

故 $1 \le x_3 \le x_2$，$P(2)$ 成立。✅

**第三步：归纳递推**

假设 $P(k)$ 成立（$k \ge 2$），即 $1 \le x_{k+1} \le x_k$。

要证 $P(k+1)$：$1 \le x_{k+2} \le x_{k+1}$。

先证 $x_{k+2} \ge 1$：

$$
x_{k+2} = \frac{1}{2}\left(x_{k+1} + \frac{1}{x_{k+1}}\right)
\ge \sqrt{x_{k+1} \cdot \frac{1}{x_{k+1}}} = 1 \quad (\text{AM–GM})
$$

再证 $x_{k+2} \le x_{k+1}$：

$$
x_{k+2} - x_{k+1}
= \frac{1}{2}\left(x_{k+1} + \frac{1}{x_{k+1}}\right) - x_{k+1}
= \frac{1 - x_{k+1}^2}{2x_{k+1}}
$$

由归纳假设 $x_{k+1} \ge 1$，故 $1 - x_{k+1}^2 \le 0$，从而 $x_{k+2} - x_{k+1} \le 0$。

因此 $1 \le x_{k+2} \le x_{k+1}$，$P(k+1)$ 成立。✅

**第四步：由归纳原理**

对一切 $n \ge 2$ 有 $1 \le x_{n+1} \le x_n$，即 $\{x_n\}_{n\ge 2}$ 单调递减有下界 ⇒ 极限存在。

设 $\displaystyle\lim_{n\to\infty} x_n = a$（$a \ge 1$），对递推式两边取极限：

$$
a = \frac{1}{2}\left(a + \frac{1}{a}\right)
\;\Longrightarrow\; 2a = a + \frac{1}{a}
\;\Longrightarrow\; a = \frac{1}{a}
\;\Longrightarrow\; a^2 = 1
$$

由 $a \ge 1$ 得 $a = 1$。

> ✅ **答案：$\boxed{1}$**

---

**解法四：定积分定义（Riemann 和与积分比较法）**

**前提**：前已证明 $\{x_n\}$ 单调递减且 $x_n \ge 1$（$n \ge 2$）。

考虑辅助函数 $f(t) = \dfrac{2t}{t^2-1}$（$t > 1$），

$$
f'(t) = \frac{2(t^2-1) - 2t\cdot 2t}{(t^2-1)^2}
= -\frac{2t^2+2}{(t^2-1)^2} < 0
$$

故 $f(t)$ 在 $(1, \infty)$ 上**严格递减**。

对 $k \ge 2$，取区间 $[x_{k+1}, x_k]$（注意 $x_{k+1} \le x_k$），由 $f$ 递减知：**右端点 $x_k$ 处的矩形面积不超过曲边梯形面积**，即

$$
f(x_k) \cdot (x_k - x_{k+1})
\; \le \; \int_{x_{k+1}}^{x_k} f(t)\,dt
$$

分别计算左右两边：

**左边**：由 $x_{k+1} = \dfrac{1}{2}\bigl(x_k + \dfrac{1}{x_k}\bigr)$ 得

$$
x_k - x_{k+1} = x_k - \frac{1}{2}\Bigl(x_k + \frac{1}{x_k}\Bigr)
= \frac{x_k^2 - 1}{2x_k}
$$

因此

$$
f(x_k)(x_k - x_{k+1})
= \frac{2x_k}{x_k^2-1} \cdot \frac{x_k^2-1}{2x_k}
= 1
$$

**右边**是精确积分：

$$
\int_{x_{k+1}}^{x_k} \frac{2t}{t^2-1}\,dt
= \Bigl[\ln(t^2-1)\Bigr]_{x_{k+1}}^{x_k}
= \ln\frac{x_k^2-1}{x_{k+1}^2-1}
$$

由不等式 $1 \le \ln\dfrac{x_k^2-1}{x_{k+1}^2-1}$ 得

$$
\frac{x_k^2-1}{x_{k+1}^2-1} \ge e
\quad\Longrightarrow\quad
x_{k+1}^2 - 1 \le e^{-1}\,(x_k^2 - 1)
$$

从 $k = 2$ 开始递推（$n \ge 2$）：

$$
x_n^2 - 1 \le (x_2^2 - 1)\,e^{-(n-2)}
$$

由夹逼准则，$\displaystyle\lim_{n\to\infty} (x_n^2 - 1) = 0$，故

$$
\lim_{n\to\infty} x_n = 1
$$

> ✅ **答案：$\boxed{1}$**

---

> 💡 **启示与要点**：
> 1. **递推数列极限的标准流程**：证单调 → 证有界 → 设极限 → 递推式取极限 → 解方程。
> 2. 本题是牛顿迭代法求 $\sqrt{1}$（即求 $x^2 = 1$ 的根）的经典例子，迭代公式 $x_{n+1} = \frac{1}{2}(x_n + \frac{a}{x_n})$ 用于求 $\sqrt{a}$。
> 3. 解法二揭示了本题的**平方收敛速度**，比解法一的"存在性 + 极限值"给出更多信息。
> 4. **数学归纳法**（解法三）适合处理**递推关系明确的单调有界证明**：将"有界性"和"单调性"统一在同一个归纳假设中，一步到位，逻辑严谨。
> 5. **定积分定义**（解法四）核心思路：利用单调函数 Riemann 和与定积分的比较关系，将递推式转化为指数衰减不等式 $x_n^2-1 \le C e^{-n}$，比单调有界准则多给出了**收敛速度**的信息。

---

### 例题：数列极限·保号性辨析

> **题目**：设 $\displaystyle\lim_{n\to\infty} a_n = a$，且 $a \neq 0$，则当 $n$ 充分大时必有（ ）
>
> A. $|a_n| > \dfrac{a}{2}$　　　　B. $|a_n| < \dfrac{a}{2}$
> C. $a_n > a - \dfrac{1}{n}$　　　　D. $a_n < a + \dfrac{1}{n}$

**思路分析**：

本题考查数列极限的**保号性**。核心工具是极限的 $\varepsilon$-$N$ 定义与三角不等式。取 $\varepsilon = \dfrac{|a|}{2}$ 将 $a_n$ 限制在 $a$ 的邻域内，再结合 $a$ 的正负分类讨论。

---

**解法**：

由 $\displaystyle\lim_{n\to\infty} a_n = a$，取 $\varepsilon = \dfrac{|a|}{2} > 0$，则 $\exists N$，当 $n > N$ 时：

$$
|a_n - a| < \frac{|a|}{2}
$$

即：

$$
a - \frac{|a|}{2} < a_n < a + \frac{|a|}{2}
$$

---

**逐项判断选项**：

**A.** $|a_n| > \dfrac{a}{2}$

由反向三角不等式 $|a_n - a| \ge |a| - |a_n|$ 得：

$$
|a_n| \ge |a| - |a_n - a| > |a| - \frac{|a|}{2} = \frac{|a|}{2}
$$

又 $\dfrac{|a|}{2} \ge \dfrac{a}{2}$（$a>0$ 时取等，$a<0$ 时 $\dfrac{|a|}{2}>0>\dfrac{a}{2}$），故：

$$
|a_n| > \frac{|a|}{2} \ge \frac{a}{2} \;\Longrightarrow\; |a_n| > \frac{a}{2}
$$

**A 恒成立 ✅**

**B.** $|a_n| < \dfrac{a}{2}$

- 若 $a > 0$：由保号性知 $|a_n| > \dfrac{a}{2}$（见 A 的推导），故不成立 ❌
- 若 $a < 0$：$\dfrac{a}{2} < 0$，而 $|a_n| \ge 0$，$|a_n| <$ 负数不可能 ❌

**B 恒不成立 ❌**

**C.** $a_n > a - \dfrac{1}{n}$

反例：取 $a_n = a - \dfrac{2}{n}$，则 $\displaystyle\lim_{n\to\infty} a_n = a$，但 $a_n = a - \dfrac{2}{n} < a - \dfrac{1}{n}$ ❌

**D.** $a_n < a + \dfrac{1}{n}$

反例：取 $a_n = a + \dfrac{2}{n}$，则 $\displaystyle\lim_{n\to\infty} a_n = a$，但 $a_n = a + \dfrac{2}{n} > a + \dfrac{1}{n}$ ❌

---

> ✅ **答案：A（$|a_n| > \dfrac{a}{2}$）**

---

> 💡 **启示与要点**：
> 1. **保号性核心**：$\displaystyle\lim a_n = a \neq 0$ ⇒ 存在 $N$，当 $n > N$ 时 $a_n$ 与 $a$ 同号，且 $|a_n| > \dfrac{|a|}{2}$。
> 2. **本题关键**：反向三角不等式 $|a_n| \ge |a| - |a_n - a|$ 直接给出 $|a_n| > \dfrac{|a|}{2}$，再由 $\dfrac{|a|}{2} \ge \dfrac{a}{2}$ 得 $|a_n| > \dfrac{a}{2}$，无须分类讨论。
> 3. **取 $\varepsilon$ 的技巧**：取 $\varepsilon = \dfrac{|a|}{2}$ 是最常用的保号性证明手法。
> 4. **常见干扰项**：C、D 中 $\dfrac{1}{n}$ 随 $n$ 变化，不能由极限定义直接保证。

---

### 例题：数列极限·乘积极限性质辨析

> **题目**：设数列 $\{x_n\}$、$\{y_n\}$ 满足 $\displaystyle\lim_{n\to\infty} x_n y_n = 0$，则下列命题正确的是（ ）
>
> A. 若 $\{x_n\}$ 发散，则 $\{y_n\}$ 必发散
> B. 若 $\{x_n\}$ 有界，则 $\{y_n\}$ 必为无穷小
> C. 若 $\{x_n\}$ 无界，则 $\{y_n\}$ 必有界
> D. 若 $\dfrac{1}{x_n}$ 为无穷小，则 $y_n$ 必为无穷小

**思路分析**：

本题考查已知 $x_n y_n \to 0$ 条件下，对各数列性质的推理。核心方法是**构造反例**排除错误选项，对正确选项给出严格证明。

---

**逐项分析**：

**A.** 若 $\{x_n\}$ 发散，则 $\{y_n\}$ 必发散

> 反例：$x_n = n$（发散），$y_n = \dfrac{1}{n^2}$（收敛于 $0$），
> 则 $x_n y_n = \dfrac{1}{n} \to 0$，但 $y_n$ 收敛。 ❌

**B.** 若 $\{x_n\}$ 有界，则 $\{y_n\}$ 必为无穷小

> 反例：$x_n = \dfrac{1}{n}$（有界），$y_n = 1$（不是无穷小），
> 则 $x_n y_n = \dfrac{1}{n} \to 0$，但 $y_n \equiv 1$ 不是无穷小。 ❌

**C.** 若 $\{x_n\}$ 无界，则 $\{y_n\}$ 必有界

> 反例：构造两个在奇偶项上"错峰"的数列
>
> $$
> x_n = \begin{cases}
> n, & n \text{ 为奇数} \\[2pt]
> 0, & n \text{ 为偶数}
> \end{cases}
> \qquad
> y_n = \begin{cases}
> 0, & n \text{ 为奇数} \\[2pt]
> n, & n \text{ 为偶数}
> \end{cases}
> $$
>
> - $x_n$ 无界（奇数次项 $n \to \infty$）✅
> - $y_n$ 无界（偶数次项 $n \to \infty$）✅
> - $x_n y_n = 0$（恒为零）$\to 0$ ✅
>
> 故 $y_n$ 可以无界。 ❌

**D.** 若 $\dfrac{1}{x_n}$ 为无穷小，则 $y_n$ 必为无穷小

> $\dfrac{1}{x_n}$ 为无穷小 $\Rightarrow |x_n| \to \infty$（$x_n$ 为无穷大量）。
>
> 由已知 $x_n y_n \to 0$，得：
>
> $$
> |y_n| = \frac{|x_n y_n|}{|x_n|} \to \frac{0}{\infty} = 0
> $$
>
> 故 $y_n \to 0$，即 $y_n$ 为无穷小。 ✅

---

> ✅ **答案：D**

---

> 💡 **启示与要点**：
> 1. **构造反例技巧**：在奇偶项上"错峰"赋值（一项很大、另一项为 $0$），是构造乘积为 $0$ 但每项无界/发散的常用手法。
> 2. **无穷小的倒数**：$\dfrac{1}{x_n}$ 为无穷小 $\iff$ $|x_n| \to \infty$（$x_n$ 为无穷大）。
> 3. **核心推理**：若 $x_n y_n \to 0$ 且 $|x_n| \to \infty$，则 $y_n = \dfrac{x_n y_n}{x_n} \to 0$，这是"有界量 × 无穷小 = 无穷小"的逆用。
> 4. **选项 B 的陷阱**：$x_n$ 有界只能推出 $x_n y_n \to 0$ 中的 $y_n$ 未必无穷小——因为 $x_n$ 本身可能趋近于 $0$（如 $x_n = \dfrac{1}{n}$），此时即使 $y_n$ 不趋近于 $0$，乘积仍可趋近于 $0$。

---

### 例题：ε-N 定义辨析·命题真伪判断

> **题目**：给出以下 4 个命题
>
> ① 若 $\displaystyle\lim_{n\to\infty} a_n = a$，则当 $n$ 充分大时，$|a_n - a| < \dfrac{1}{1000!}$
>
> ② 若 $\displaystyle\lim_{n\to\infty} a_n = a$，则对任意给定的 $\varepsilon > 0$，当 $n$ 充分大时，$|a_n - a| < \dfrac{\varepsilon}{100}$
>
> ③ 若 $\displaystyle\lim_{n\to\infty} a_n = a$，则对任意给定的 $\varepsilon > 0$，当 $n$ 充分大时，$|a_n - a| < 100\varepsilon$
>
> ④ 若 $\displaystyle\lim_{n\to\infty} a_n = a$，则当 $n$ 充分大时，$|a_n - a| < \dfrac{1000!}{n}$
>
> 其中真命题个数为（ ）
>
> A. 0　　　B. 1　　　C. 2　　　D. 3

**思路分析**：

本题考察对 **ε-N 定义** 的理解。核心是判断每个条件是否可由 $\displaystyle\lim_{n\to\infty} a_n = a$ 推出：

- 命题①④没有 $\forall\varepsilon>0$ 前缀，只需取定一个 $\varepsilon$ 即可
- 命题②③带"对任意 $\varepsilon>0$"，判断其是否等价于原定义

---

**逐项判断**：

**①** $|a_n - a| < \dfrac{1}{1000!}$

在极限定义中取 $\varepsilon = \dfrac{1}{1000!} > 0$，则 $\exists N$，当 $n\ge N$ 时 $|a_n-a|<\varepsilon = \dfrac{1}{1000!}$。

> ✅ **正确**

---

**②** $|a_n - a| < \dfrac{\varepsilon}{100}$

对任意 $\varepsilon > 0$，令 $\varepsilon' = \dfrac{\varepsilon}{100} > 0$，由极限定义 $\exists N$，$n\ge N \Rightarrow |a_n-a|<\varepsilon' = \dfrac{\varepsilon}{100}$。

> ✅ **正确**

---

**③** $|a_n - a| < 100\varepsilon$

对任意 $\varepsilon > 0$，$100\varepsilon$ 也是任意正数，由极限定义直接得证。

> ✅ **正确**

---

**④** $|a_n - a| < \dfrac{1000!}{n}$

取反例：$a_n = a + \dfrac{1}{\sqrt{n}}$，则 $a_n \to a$，但 $|a_n-a| = \dfrac{1}{\sqrt{n}}$。

当 $n$ 足够大时，$\sqrt{n} > 1000!$，即 $\dfrac{1}{\sqrt{n}} < \dfrac{1000!}{n}$ 不成立（因为 $\dfrac{1}{\sqrt{n}} > \dfrac{1000!}{n} \iff \sqrt{n} < 1000!$ 对 $n < (1000!)^2$ 不成立）。

实际上 $\dfrac{1}{\sqrt{n}} > \dfrac{1000!}{n}$ 等价于 $\sqrt{n} < 1000!$，当 $n > (1000!)^2$ 时不等式反向，从而 $|a_n-a| > \dfrac{1000!}{n}$，该条件不满足。

> ❌ **错误**

---

| 命题 | 结果 | 理由 |
|:---:|:---:|:---|
| ① | ✅ | 取 $\varepsilon = 1/1000!$ 即得 |
| ② | ✅ | $\varepsilon/100$ 可替换原定义中的 $\varepsilon$ |
| ③ | ✅ | $100\varepsilon$ 也可替换原定义中的 $\varepsilon$ |
| ④ | ❌ | 反例 $a_n = a + 1/\sqrt{n}$ 不满足该不等式 |

3 个正确。

> ✅ **答案：D（3 个）**

---

> 💡 **启示与要点**：
> 1. **①②③ 的本质**：极限定义中的 $\varepsilon$ 可以是任意正数，无论乘除多少倍，都等价于原定义。
> 2. **④ 的陷阱**：分母有 $n$ 的不等式并非 $\varepsilon$-$N$ 定义的直接推论，它要求收敛速度——不是所有收敛数列都满足。
> 3. **判断标准**：看到具体数字（如 $1/1000!$）→ 取 $\varepsilon$ 等于该数字即可；看到 $\varepsilon$ 的倍数 → 本质上与定义等价；看到含 $n$ 的表达式 → 警惕收敛速度条件。

---

### 例题：数列极限 · 比值判别法 + $\frac{a^n n!}{n^n}$ 型

> **题目**：数列极限中一个常用结论：
>
> (1) 若 $\lim\limits_{n\to\infty}\dfrac{a_{n+1}}{a_n}=a$ 且 $|a|<1$，则 $\lim\limits_{n\to\infty}a_n=0$；
>
> (2) 利用 (1) 证明：$\displaystyle\lim_{n\to\infty}\dfrac{2^n n!}{n^n}=0$，$\displaystyle\lim_{n\to\infty}\dfrac{3^n n!}{n^n}=+\infty$。

**思路分析**：

本题考察**数列的比值判别法**——类比正项级数的比值判别法，但直接用于数列收敛性。对 $\frac{a^n n!}{n^n}$ 型数列，直接求极限很难，但相邻项比值可借助重要极限 $\lim(1+\frac{1}{n})^n=e$ 化简。

---

**(1) 比值判别法原理**：

当 $\lim\frac{a_{n+1}}{a_n}=a$ 且 $|a|<1$ 时，$|a_n|$ 最终按几何级数速度衰减，必有 $a_n\to0$。

> 直观：若 $\frac{a_{n+1}}{a_n}\approx a<1$，则 $a_n\approx C\cdot a^n\to0$。

---

**(2) 令 $a_n=\dfrac{a^n n!}{n^n}$，求相邻项比值**：

$$
\begin{aligned}
\frac{a_{n+1}}{a_n}
&= \frac{\dfrac{a^{n+1}(n+1)!}{(n+1)^{n+1}}}{\dfrac{a^n n!}{n^n}}
= a \cdot \frac{(n+1)!}{n!} \cdot \frac{n^n}{(n+1)^{n+1}} \\[6pt]
&= a \cdot (n+1) \cdot \frac{n^n}{(n+1)^n \cdot (n+1)} \\[6pt]
&= a \cdot \frac{n^n}{(n+1)^n}
= a \cdot \left(\frac{n}{n+1}\right)^n \\[6pt]
&= \frac{a}{\left(1+\frac{1}{n}\right)^n}
\end{aligned}
$$

取极限：

$$
\lim_{n\to\infty}\frac{a_{n+1}}{a_n}
= \frac{a}{\displaystyle\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n}
= \frac{a}{e}
$$

---

**分别代入**：

| $a$ 的值 | $\displaystyle\lim\frac{a_{n+1}}{a_n}=\frac{a}{e}$ | 与 $1$ 比较 | $\lim a_n$ |
|:---:|:---|:---:|:---|
| $a=2$ | $\dfrac{2}{e}\approx 0.736$ | $<1$ ✅ | $0$ |
| $a=3$ | $\dfrac{3}{e}\approx 1.104$ | $>1$ ✅ | $+\infty$ |

> ✅ **答案**：$\displaystyle\lim_{n\to\infty}\dfrac{2^n n!}{n^n}=0$，$\displaystyle\lim_{n\to\infty}\dfrac{3^n n!}{n^n}=+\infty$

---

> 💡 **启示与要点**：
> 1. **比值判别法在数列上的应用**：若 $\lim\frac{a_{n+1}}{a_n}<1$ → $a_n\to0$；若 $>1$ → $|a_n|\to\infty$；若 $=1$ → 无法判断。
> 2. **核心极限**：$\lim(1+\frac{1}{n})^n=e$ 是化简 $\frac{n^n}{(n+1)^n}$ 型表达式的关键。
> 3. **分水岭在 $a=e$**：当 $a<e$ 时 $\frac{a^n n!}{n^n}\to0$，$a>e$ 时 $\to+\infty$。$2<e<3$ 是天然的命题素材。
> 4. 此题也可用**斯特林公式** $n!\sim\sqrt{2\pi n}\left(\frac{n}{e}\right)^n$ 直接得出，但比值法更初等、更符合考研风格。

---

## 五、无穷大 × 非零周期函数

> **知识卡片**：设 $f(x)$ 为**非零周期函数**（如 $\sin x$、$\cos x$），$g(x) \to \infty$（$x \to x_0$），则：
>
> $$
> f(x) \cdot g(x) \quad\text{是}\quad \text{【无界但不为无穷大】}
> $$
>
> **为什么不是无穷大？**
> 无穷大的定义：$\forall M > 0$，$\exists \delta > 0$，当 $0 < |x-x_0| < \delta$ 时，$|h(x)| > M$。
>
> 但 $f(x) \cdot g(x)$ 不满足此定义——因为 $f(x)$ 周期性振荡，会**反复穿过零点**：
> - 当周期函数取 $\pm 1$ 时：$|f \cdot g| = |g| \to \infty$（可以任意大 → **无界**）
> - 当周期函数取 $0$ 时：$f \cdot g = 0$（无法保证始终大于任意 $M$ → **不是无穷大**）
>
> **判定口诀**：无穷大 $\times$ 非零周期函数 $=$ 无界 $\neq$ 无穷大

### 例题：无穷大 × 周期函数·无界但不为无穷大（1993 数三真题）

> **题目**（例16·1993 数三）：当 $x \to 0$ 时，变量 $\displaystyle \frac{1}{x^2}\sin\frac{1}{x}$ 是（ ）
>
> A. 无穷小
> B. 无穷大
> C. 有界的，但不是无穷小
> D. 无界的，但不是无穷大

**思路分析**：

$x \to 0$ 时，$\frac{1}{x^2} \to +\infty$（无穷大量），而 $\sin\frac{1}{x}$ 在 $[-1,1]$ 间无限次振荡（周期函数）。两者的乘积既不是无穷大（因为 $\sin\frac{1}{x}$ 反复取 $0$），也不是有界（因为 $\sin\frac{1}{x}$ 反复取 $\pm 1$ 时 $\frac{1}{x^2}$ 可以任意大）。

---

**解法**：

**第一步：证明无界**

取子列 $x_n = \dfrac{1}{2n\pi + \frac{\pi}{2}}$，则当 $n \to \infty$ 时 $x_n \to 0$，且：

$$
\sin\frac{1}{x_n} = \sin\left(2n\pi + \frac{\pi}{2}\right) = 1
$$

$$
\frac{1}{x_n^2}\sin\frac{1}{x_n} = \frac{1}{x_n^2} \times 1 = \left(2n\pi + \frac{\pi}{2}\right)^2 \to +\infty
$$

所以该变量**无界** ✅

---

**第二步：证明不是无穷大**

取另一子列 $x_n = \dfrac{1}{2n\pi}$，则当 $n \to \infty$ 时 $x_n \to 0$，且：

$$
\sin\frac{1}{x_n} = \sin(2n\pi) = 0
$$

$$
\frac{1}{x_n^2}\sin\frac{1}{x_n} = \frac{1}{x_n^2} \times 0 = 0
$$

在 $x=0$ 的任意邻域内，该变量都能取到 $0$，不满足无穷大的定义（无穷大要求「最终」恒大于任意正数），所以**不是无穷大** ❌

---

**结论**：无界但不是无穷大。

> ✅ **答案：D**

---

### 🧪 配套练习

> **练习1**：当 $x \to \infty$ 时，$x\sin x$ 是（ ）
>
> A. 无穷小　B. 无穷大　C. 有界变量　D. 无界但非无穷大

**解**：$x \to \infty$，$\sin x$ 振荡于 $[-1,1]$。

- 取 $x = 2n\pi + \frac{\pi}{2}$，$x\sin x = x \to \infty$ → 无界
- 取 $x = n\pi$，$x\sin x = 0$ → 不是无穷大

> **答案**：D

---

> **练习2**：当 $x \to 0$ 时，$\displaystyle \frac{1}{x}\cos\frac{1}{x}$ 是（ ）

**解**：同理，$\frac{1}{x} \to \infty$，$\cos\frac{1}{x}$ 振荡。

- 取 $x = \frac{1}{2n\pi}$，$\cos\frac{1}{x} = 1$，$\frac{1}{x}\cos\frac{1}{x} = 2n\pi \to \infty$ → 无界
- 取 $x = \frac{1}{2n\pi + \frac{\pi}{2}}$，$\cos\frac{1}{x} = 0$，表达式 $=0$ → 不是无穷大

> **答案**：无界但不是无穷大

---

> 💡 **启示**：
> - **无界 ≠ 无穷大**：无穷大要求「终极」大于任意数，无界只要求「存在」大于任意数的点
> - 判断方法：构造两个子列——一个使周期函数取 $\pm 1$（证无界），一个使周期函数取 $0$（证非无穷大）
> - 常见 $\sin\frac{1}{x}$ 在 $x\to 0$ 时的振荡是此类题的标志性信号
> - 经典结论：$\frac{1}{x^k}\sin\frac{1}{x}$（$k>0$，$x\to 0$）永远是无界但非无穷大

---

## 六、复合函数反推内层极限

> **知识卡片**：设 $\displaystyle\lim_{x \to x_0} f(g(x)) = A$，且满足：
>
> 1. $f(u)$ **严格单调**（在 $u = \lim g(x)$ 的邻域内）
> 2. $g(x)$ **有界**
>
> 则 $\displaystyle\lim_{x \to x_0} g(x)$ 存在，且 $\lim g(x) = f^{-1}(A)$。
>
> **考研常用场景**：已知 $\lim e^{g(x)}$、$\lim \arctan g(x)$ 等复合极限存在且 $g(x)$ 有界，反推 $\lim g(x)$。

### 例题：复合函数反推内层极限

> **题目**：设 $f(x)$ 在 $\mathbb{R}$ 上连续且严格单调递增，$\displaystyle\lim_{x \to +\infty} f(g(x)) = A$，且 $g(x)$ 在 $[0,+\infty)$ 上有界。证明：$\displaystyle\lim_{x \to +\infty} g(x)$ 存在，并求出该极限。

**思路分析**：

外层 $f$ 严格单调递增 + 内层 $g(x)$ 有界 → 反推 $g(x)$ 极限存在。再利用 $f$ 的连续性，极限可"穿透"：$f(\lim g) = \lim f(g) = A$，进而 $\lim g = f^{-1}(A)$。

---

**解法**：

**第一步：证明 $\lim g(x)$ 存在**

$g(x)$ 有界，由 Bolzano-Weierstrass 定理，$g(x)$ 必有收敛子列。

用反证法。假设 $\lim g(x)$ 不存在，则存在两个子列：

$$
g(x_{n_k}) \to \alpha,\quad g(x_{m_k}) \to \beta,\quad \alpha \neq \beta
$$

由于 $f$ 连续，对第一个子列：

$$
f(g(x_{n_k})) \to f(\alpha)
$$

对第二个子列：

$$
f(g(x_{m_k})) \to f(\beta)
$$

又已知 $\lim f(g(x)) = A$，故 $f(\alpha) = f(\beta) = A$。

但 $f$ **严格单调**，所以 $f$ 是单射，$f(\alpha) = f(\beta)$ 推出 $\alpha = \beta$，与假设矛盾。

因此 $\lim g(x)$ 存在 ✅

---

**第二步：求极限值**

设 $\displaystyle\lim_{x \to +\infty} g(x) = L$，由 $f$ 连续：

$$
\lim_{x \to +\infty} f(g(x)) = f\!\left(\lim_{x \to +\infty} g(x)\right) = f(L)
$$

又已知 $\lim f(g(x)) = A$，所以：

$$
f(L) = A \quad\Rightarrow\quad L = f^{-1}(A)
$$

> ✅ **答案**：$\displaystyle\lim_{x \to +\infty} g(x) = f^{-1}(A)$

---

### 🧪 配套练习

> **练习1**：设 $\displaystyle\lim_{x \to 0} \arctan(g(x)) = \frac{\pi}{4}$，且 $g(x)$ 在 $x=0$ 附近有界，求 $\displaystyle\lim_{x \to 0} g(x)$。

**解**：$\arctan$ 严格单调递增，$g(x)$ 有界 ⇒ $\lim g(x)$ 存在。

$$
\arctan(\lim g) = \frac{\pi}{4} \quad\Rightarrow\quad \lim g = \tan\frac{\pi}{4} = 1
$$

> **答案**：$1$

---

> **练习2**：设 $\displaystyle\lim_{x \to \infty} \ln(g(x)) = 0$，且 $g(x) > 0$ 有界，求 $\displaystyle\lim_{x \to \infty} g(x)$。

**解**：$\ln$ 严格单调递增，$g(x)$ 有界 ⇒ $\lim g(x)$ 存在。

$$
\ln(\lim g) = 0 \quad\Rightarrow\quad \lim g = e^0 = 1
$$

> **答案**：$1$

---

> 💡 **启示**：
> - 复合函数反推内层极限的三要素：**复合极限存在 + 外层严格单调 + 内层有界**
> - 证明核心：有界 ⇒ 子列收敛，单调性 ⇒ 不同极限点不可能
> - 考研常见外层函数：$e^x$、$\ln x$、$\arctan x$、$x^3$ 等严格单调函数
> - 条件缺一不可：外层不单调或内层无界都可能反例

---

### 例题：单调性判定·复合函数反推（2022 数一/二真题）

> **题目**（例15·2022 数一、二）：已知数列 $\{x_n\}$，其中 $-\dfrac{\pi}{2} \leq x_n \leq \dfrac{\pi}{2}$，则（ ）
>
> A. 当 $\displaystyle\lim_{n\to\infty}\cos(\sin x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}x_n$ 存在
> B. 当 $\displaystyle\lim_{n\to\infty}\sin(\cos x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}x_n$ 存在
> C. 当 $\displaystyle\lim_{n\to\infty}\cos(\sin x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}\sin x_n$ 存在，但 $\displaystyle\lim_{n\to\infty}x_n$ 不一定存在
> D. 当 $\displaystyle\lim_{n\to\infty}\sin(\cos x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}\cos x_n$ 存在，但 $\displaystyle\lim_{n\to\infty}x_n$ 不一定存在

**思路分析**：

本题是**复合函数反推内层极限**定理的应用，四个选项全是 sin/cos 两层嵌套。核心判断：

| 函数 | 在对应区间上的单调性 |
|:---|:---|
| $\sin x$ 在 $[0,1]$ 上 | ✅ **严格单调递增** |
| $\cos x$ 在 $[-1,1]$ 上 | ❌ 偶函数，$\cos(-t)=\cos t$，不单调 |

**关键结论**：
- 外层 $\sin$ + 内层 $\cos x_n \in [0,1]$ → 单调 → **可反推** $\lim\cos x_n$ 存在
- 外层 $\cos$ + 内层 $\sin x_n \in [-1,1]$ → 不单调 → **不可反推**

---

**逐项分析**：

**选项 A**：$\lim\cos(\sin x_n)$ 存在 ⇒ $\lim x_n$ 存在？

- 外层 $\cos$ 不单调 → 无法反推
- 🧪 反例：$x_n = (-1)^n \cdot \frac{\pi}{2}$，$\cos(\sin x_n) \equiv \cos 1$（存在），但 $x_n$ 振荡
- ❌ **A 错**

**选项 B**：$\lim\sin(\cos x_n)$ 存在 ⇒ $\lim x_n$ 存在？

- 外层 $\sin$ 单调 → 可推出 $\lim\cos x_n$ 存在
- 但 $\cos$ 不单调 → $\lim\cos x_n$ 存在推不出 $\lim x_n$ 存在
- 🧪 反例：$x_n = (-1)^n \cdot \frac{\pi}{3}$，$\sin(\cos x_n) \equiv \sin\frac{1}{2}$（存在），但 $x_n$ 振荡
- ❌ **B 错**

**选项 C**：$\lim\cos(\sin x_n)$ 存在 ⇒ $\lim\sin x_n$ 存在？

- 前提：$\lim\cos(\sin x_n)$ 存在；结论：$\lim\sin x_n$ 存在
- 外层 $\cos$ 不单调 → 复合极限存在 **不能推出** 内层 $\sin x_n$ 极限存在！
- 🧪 反例：$x_n = (-1)^n \cdot \frac{\pi}{2}$，$\sin x_n = (-1)^n$（振荡 ❌），但 $\cos(\sin x_n) \equiv \cos 1$（存在 ✅）
- ❌ **C 错**（结论本身就错了）

**选项 D**：$\lim\sin(\cos x_n)$ 存在 ⇒ $\lim\cos x_n$ 存在，但 $\lim x_n$ 不一定？

- 外层 $\sin$ 单调 + 内层 $\cos x_n \in [0,1]$ 有界 + 复合极限存在
- ✅ 定理直接命中：$\lim\cos x_n$ 存在
- 且 $\cos$ 不单调 → $\lim x_n$ 确实不一定存在
- 🧪 验证：$x_n = (-1)^n \cdot \frac{\pi}{3}$，$\cos x_n \equiv \frac{1}{2}$（存在 ✅），$x_n$ 振荡（不存在 ✅）
- ✅ **D 对！**

---

> ✅ **答案：D**

**💡 启示**：

- A 和 C **前提相同**（$\cos(\sin x_n)$），B 和 D **前提相同**（$\sin(\cos x_n)$）
- 唯一能用定理的是 D：$\sin$ 单调 → $\cos x_n$ 收敛；但 $\cos$ 不单调 → $x_n$ 未必收敛
- C 是最大陷阱：外层 $\cos$ 不单调，复合极限存在 ≠ 内层极限存在

📐 **图示**：

```
  -π/2        0        π/2
    ├─────────┼─────────┤
sin:  ↗ -1 → 0 → 1 ↗    (严格单调 ✅)
cos:  ↘ 0 → 1 → 0 ↘    (非单调 ❌)

sin x_n ∈ [-1,1]  → cos 不单调 → A、C 不可反推
cos x_n ∈ [0,1]   → sin 单调   → B、D 可推到 cos x_n
                                   B 过度推断到 x_n ❌
                                   D 恰在 cos x_n 停住 ✅
```

---

## 七、$\infty-\infty$ 型极限

### 例题：$\infty-\infty$ 型 · 提取 + 泰勒展开

> **题目**（题型二·5）：求 $\displaystyle\lim_{x\to+\infty}\left[\frac{x^{1+x}}{(1+x)^x} - \frac{x}{e}\right]$

**思路分析**：

$x\to+\infty$ 时，两项都趋于 $+\infty$，属于 $\infty-\infty$ 型。首先要将第一项重写为更易展开的形式，核心是处理 $(1+\frac{1}{x})^x \to e$，并展开到足够阶数以消去主项、露出差值。

---

**第一步：重写第一项**

$$
\frac{x^{1+x}}{(1+x)^x}
= x \cdot \frac{x^x}{(1+x)^x}
= x \cdot \left(\frac{x}{1+x}\right)^x
= x \cdot \left(\frac{1}{1+\frac{1}{x}}\right)^x
$$

令 $t = \frac{1}{x}$，则 $x\to+\infty \iff t\to0^+$：

$$
x \cdot \left(\frac{1}{1+\frac{1}{x}}\right)^x
= \frac{1}{t} \cdot \left(\frac{1}{1+t}\right)^{1/t}
$$

---

**第二步：展开 $(1+t)^{1/t}$（关键）**

$$
\begin{aligned}
(1+t)^{1/t}
&= e^{\frac{\ln(1+t)}{t}} \\
&= e^{\frac{t - \frac{t^2}{2} + \frac{t^3}{3} + O(t^4)}{t}} \\
&= e^{1 - \frac{t}{2} + \frac{t^2}{3} + O(t^3)} \\
&= e \cdot e^{-\frac{t}{2} + \frac{t^2}{3} + O(t^3)} \\
&= e \cdot \left[1 + \left(-\frac{t}{2} + \frac{t^2}{3}\right) + \frac{1}{2}\left(-\frac{t}{2}\right)^2 + O(t^3)\right] \\
&= e \cdot \left[1 - \frac{t}{2} + \frac{t^2}{3} + \frac{t^2}{8} + O(t^3)\right] \\
&= e \cdot \left[1 - \frac{t}{2} + \frac{11}{24}t^2 + O(t^3)\right]
\end{aligned}
$$

---

**第三步：取倒数展开**

$$
\begin{aligned}
\left(\frac{1}{1+t}\right)^{1/t}
&= \frac{1}{(1+t)^{1/t}}
= \frac{1}{e\left[1 - \frac{t}{2} + \frac{11}{24}t^2 + O(t^3)\right]} \\
&= \frac{1}{e} \cdot \left[1 + \frac{t}{2} + O(t^2)\right] \quad\text{（}\frac{1}{1-u}=1+u+\cdots\text{）}\\
&= \frac{1}{e} + \frac{t}{2e} + O(t^2)
\end{aligned}
$$

---

**第四步：代回求极限**

$$
\begin{aligned}
\frac{x^{1+x}}{(1+x)^x}
&= \frac{1}{t} \cdot \left(\frac{1}{e} + \frac{t}{2e} + O(t^2)\right) \\
&= \frac{1}{e \cdot t} + \frac{1}{2e} + O(t) \\
&= \frac{x}{e} + \frac{1}{2e} + o(1) \quad(\because\; t=\tfrac{1}{x})
\end{aligned}
$$

---

**第五步：相减**

$$
\lim_{x\to+\infty}\left[\frac{x^{1+x}}{(1+x)^x} - \frac{x}{e}\right]
= \lim_{x\to+\infty}\left[\frac{x}{e} + \frac{1}{2e} + o(1) - \frac{x}{e}\right]
= \frac{1}{2e}
$$

> ✅ **答案：$\boxed{\dfrac{1}{2e}}$**

---

> 💡 **启示与要点**：
> 1. **提取主项**：$x^n$ 型比 $a^n$ 型优先——当底数和指数都有 $x$ 时，先提出 $x$ 把问题转到 $(1+1/x)^x$ 类表达式。
> 2. **$(1+t)^{1/t}$ 的泰勒展开**是这道题的核心计算量——展开到 $t^2$ 才能得到常数项。
> 3. **$\infty-\infty$ 型的套路**：重写 → 展开 → 消去主导项 → 剩下的常数就是答案。
> 4. 类似题型：$\lim(1+\frac{1}{n})^n = e$，但 $(1+\frac{1}{n})^n$ 的**二阶展开**是这道题的区分点。

---

### 例题：判断曲线的渐近线

> **题目**（2014, 数一/二）：下列曲线中有渐近线的是（ ）
>
> A. $y = x + \sin x$
> B. $y = x^2 + \sin x$
> C. $y = x + \sin\frac{1}{x}$
> D. $y = x^2 + \sin\frac{1}{x}$

**思路分析**：

渐近线分三种：**水平**（$\lim_{x\to\infty}f(x)=L$）、**垂直**（$f(x)\to\infty$ 在某点）、**斜**（$y=kx+b$，$k=\lim\frac{f(x)}{x}$，$b=\lim[f(x)-kx]$）。

本题四个选项都含 $\sin$ 振荡项，关键看极限是否存在。

---

**逐选项分析**：

| 选项 | $k = \lim\frac{f(x)}{x}$ | $b = \lim[f(x)-kx]$ | 渐近线 |
|:---|:---|:---|:---:|
| **A** | $\lim\frac{x+\sin x}{x}=1$ | $\lim\sin x$ **不存在**（振荡） | ❌ |
| **B** | $\lim\frac{x^2+\sin x}{x}=\infty$ | — | ❌ |
| **C** | $\lim\frac{x+\sin\frac{1}{x}}{x}=1$ | $\lim\sin\frac{1}{x}=0$ ✅ | ✅ $y=x$ |
| **D** | $\lim\frac{x^2+\sin\frac{1}{x}}{x}=\infty$ | — | ❌ |

---

**关键对比**：

| | $\sin x$（A/B） | $\sin\frac{1}{x}$（C/D） |
|:---|:---|:---|
| $x\to\infty$ 时 | 振荡无极限 | $\frac{1}{x}\to0$，$\sin\frac{1}{x}\to0$ |
| 斜渐近线 $b$ 是否存在 | ❌ 不存在 | ✅ 存在，等于 0 |

---

> ✅ **答案：C**，渐近线为 $y = x$

**💡 启示**：

| 要点 | 说明 |
|:---|:---|
| $\sin x$ vs $\sin\frac{1}{x}$ | $x\to\infty$ 时前者振荡无极限，后者趋于 0——这是本题的核心区分 |
| 求斜渐近线的两步 | 先求 $k$，$k$ 存在且非零有限时才求 $b$；$k$ 不存在或为 $\infty$ 则直接排除 |
| 含振荡项的处理 | 若振荡项在 $x\to\infty$ 时趋于 0（如 $\sin\frac{1}{x}$），则不影响渐近线 |

---

> 📎 **关联文件**：[泰勒展开与等价无穷小](/Math/calculus_taylor) | [洛必达法则失效](/Math/calculus_lhopital) | [连续与间断点](/Math/calculus_continuous) | [返回考研总览](/)
