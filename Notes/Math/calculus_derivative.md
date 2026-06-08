# 常用求导公式（一元函数微分学）

> 📌 **本章内容**：基本初等函数求导、四则运算、链式法则、隐函数、参数方程、对数求导、高阶导数、反函数、分段函数、变限积分求导

---

## 一、基本初等函数求导公式

| 函数 | 导数 | 记忆要点 |
|:---|:---|:---:|
| $C$（常数） | $0$ | — |
| $x^\mu$（$\mu\in\mathbb{R}$） | $\mu x^{\mu-1}$ | 指数提前，指数减一 |
| $a^x$（$a>0$） | $a^x \ln a$ | 自身 $\times \ln a$ |
| $e^x$ | $e^x$ | 不变，最特殊的指数函数 |
| $\log_a x$（$a>0,a\neq1$） | $\dfrac{1}{x\ln a}$ | 分母多 $\ln a$ |
| $\ln x$ | $\dfrac{1}{x}$ | — |
| $\sin x$ | $\cos x$ | 余函数 |
| $\cos x$ | $-\sin x$ | 负的正弦 |
| $\tan x$ | $\sec^2 x = \dfrac{1}{\cos^2 x}$ | 正割平方 |
| $\cot x$ | $-\csc^2 x = -\dfrac{1}{\sin^2 x}$ | 负的余割平方 |
| $\sec x$ | $\sec x \tan x$ | 自身 $\times \tan x$ |
| $\csc x$ | $-\csc x \cot x$ | 负的自身 $\times \cot x$ |
| $\arcsin x$ | $\dfrac{1}{\sqrt{1-x^2}}$ | — |
| $\arccos x$ | $-\dfrac{1}{\sqrt{1-x^2}}$ | 与 $\arcsin x$ 相反数 |
| $\arctan x$ | $\dfrac{1}{1+x^2}$ | — |
| $\operatorname{arccot} x$ | $-\dfrac{1}{1+x^2}$ | 与 $\arctan x$ 相反数 |

> 💡 **记忆口诀**：
> - **正弦余弦**：$\sin$ 求导变 $\cos$，$\cos$ 求导变 $-\sin$
> - **正割余割**：$\sec$ 求导 $\sec\tan$，$\csc$ 求导 $-\csc\cot$
> - **反三角**：$\arcsin$ 和 $\arccos$ 分母 $\sqrt{1-x^2}$，符号相反；$\arctan$ 和 $\operatorname{arccot}$ 分母 $1+x^2$，符号相反

---

## 二、四则运算法则

| 法则 | 公式 |
|:---|:---|
| **和差** | $(u \pm v)' = u' \pm v'$ |
| **乘法** | $(uv)' = u'v + uv'$ |
| **数乘** | $(Cu)' = Cu'$ |
| **除法** | $\left(\dfrac{u}{v}\right)' = \dfrac{u'v - uv'}{v^2}\;(v\neq0)$ |

> **推广（莱布尼茨公式）**：$(uv)^{(n)} = \displaystyle\sum_{k=0}^{n} C_n^k u^{(n-k)} v^{(k)}$

---

## 三、复合函数求导——链式法则（核心！）

$$
\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
\quad\text{或}\quad
[f(g(x))]' = f'(g(x)) \cdot g'(x)
$$

> **本质**：外层函数求导（内层不动）$\times$ 内层函数求导

### ⚡ 考研常用复合求导速查表

$$
\begin{aligned}
&[f(ax+b)]' = a \cdot f'(ax+b) \\[2pt]
&[f(x^\alpha)]' = \alpha x^{\alpha-1} \cdot f'(x^\alpha) \\[2pt]
&[e^{f(x)}]' = e^{f(x)} \cdot f'(x) \\[2pt]
&[\ln f(x)]' = \frac{f'(x)}{f(x)} \\[2pt]
&[f(x)^{g(x)}]' = f(x)^{g(x)}\left[g'(x)\ln f(x) + g(x)\frac{f'(x)}{f(x)}\right] \quad\text{（幂指函数）}
\end{aligned}
$$

---

## 四、隐函数求导法

对于方程 $F(x, y)=0$ 确定的隐函数 $y=y(x)$：

1. 方程两边同时对 $x$ 求导，将 $y$ 视为 $x$ 的函数
2. 解出 $y'$

> **公式**：若 $F(x,y)=0$ 且 $F_y\neq0$，则 $\displaystyle \frac{dy}{dx} = -\frac{F_x}{F_y}$

---

## 五、参数方程求导法

若 $y = y(t),\;x = x(t)$，则：

$$
\frac{dy}{dx} = \frac{y'(t)}{x'(t)},\qquad
\frac{d^2y}{dx^2} = \frac{y''(t)x'(t) - y'(t)x''(t)}{[x'(t)]^3}
$$

---

## 六、对数求导法

适用场景：**幂指函数**或**多个因式乘除**。

**步骤**：
1. 两边取 $\ln$
2. 隐函数求导
3. 解出 $y'$

> **典型例子**：$y = x^{\sin x}$，$\ln y = \sin x \cdot \ln x$，两边求导得 $y' = x^{\sin x}\left(\cos x \ln x + \dfrac{\sin x}{x}\right)$

---

## 七、高阶导数常用公式

| 函数 | $n$ 阶导数 |
|:---|:---:|
| $\sin x$ | $\sin\!\left(x + \dfrac{n\pi}{2}\right)$ |
| $\cos x$ | $\cos\!\left(x + \dfrac{n\pi}{2}\right)$ |
| $e^x$ | $e^x$ |
| $a^x$ | $a^x (\ln a)^n$ |
| $\ln(ax+b)$ | $(-1)^{n-1} \dfrac{(n-1)!\, a^n}{(ax+b)^n}$ |
| $\dfrac{1}{ax+b}$ | $(-1)^n \dfrac{n!\, a^n}{(ax+b)^{n+1}}$ |
| $x^\alpha$ | $\alpha(\alpha-1)\cdots(\alpha-n+1)\,x^{\alpha-n}$ |
| $f(ax+b)$ | $a^n f^{(n)}(ax+b)$ |

---

## 八、可导 $\Leftrightarrow$ 左右导数存在且相等

函数 $f(x)$ 在 $x_0$ 处可导的充要条件：

$$
f'_-(x_0) = f'_+(x_0) \quad\text{（存在且相等）}
$$

> 其中左导数 $f'_-(x_0) = \displaystyle\lim_{x\to x_0^-}\frac{f(x)-f(x_0)}{x-x_0}$，右导数 $f'_+(x_0) = \displaystyle\lim_{x\to x_0^+}\frac{f(x)-f(x_0)}{x-x_0}$

---

## 九、反函数求导法则

设 $y = f(x)$ 在区间 $I$ 上单调可导且 $f'(x) \neq 0$，其反函数 $x = \varphi(y)$ 也可导，则：

$$
\varphi'(y) = \frac{1}{f'(x)} \quad\text{或}\quad \frac{dx}{dy} = \frac{1}{\frac{dy}{dx}}
$$

> **本质**：反函数的导数 = 原函数导数的倒数

### 考研常用反函数导数对应

| 原函数 | 反函数 | 反函数导数 |
|:---|:---|:---:|
| $y = e^x$ | $x = \ln y$ | $\dfrac{dx}{dy} = \dfrac{1}{y} \;\Rightarrow\; (\ln y)' = \dfrac{1}{y}$ |
| $y = \sin x$ | $x = \arcsin y$ | $\dfrac{dx}{dy} = \dfrac{1}{\cos x} = \dfrac{1}{\sqrt{1-y^2}}$ |
| $y = \cos x$ | $x = \arccos y$ | $\dfrac{dx}{dy} = -\dfrac{1}{\sin x} = -\dfrac{1}{\sqrt{1-y^2}}$ |
| $y = \tan x$ | $x = \arctan y$ | $\dfrac{dx}{dy} = \dfrac{1}{\sec^2 x} = \dfrac{1}{1+y^2}$ |
| $y = a^x$ | $x = \log_a y$ | $\dfrac{dx}{dy} = \dfrac{1}{a^x \ln a} = \dfrac{1}{y\ln a}$ |

> 📌 **注**：反三角函数的求导公式正是利用反函数求导法则推导得出的。

---

## 十、分段函数求导

分段函数在分段点处的导数需用**导数定义**判断：

$$
f'(x_0) = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0}
$$

**步骤**：
1. 在分段点处，用定义求左导数 $f'_-(x_0)$ 和右导数 $f'_+(x_0)$
2. 若 $f'_-(x_0) = f'_+(x_0)$，则 $f'(x_0)$ 存在，否则不可导
3. 非分段点处，直接使用求导公式

> **典型例子——绝对值函数**：$f(x)=|x|$ 在 $x=0$ 处
>
> $$
> f'_-(0) = \lim_{x\to0^-}\frac{-x-0}{x-0} = -1,\quad
> f'_+(0) = \lim_{x\to0^+}\frac{x-0}{x-0} = 1
> $$
>
> 左右导数不相等，故 $|x|$ 在 $x=0$ 处**不可导**。

---

## 十一、变限积分求导（考研高频！）

若 $F(x) = \displaystyle\int_{a(x)}^{b(x)} f(t)\,dt$，其中 $f(t)$ 连续，$a(x), b(x)$ 可导，则：

$$
F'(x) = f(b(x)) \cdot b'(x) - f(a(x)) \cdot a'(x)
$$

### 常见特例

| 形式 | 导数 |
|:---|:---:|
| $\displaystyle\frac{d}{dx}\int_a^x f(t)\,dt$ | $f(x)$ |
| $\displaystyle\frac{d}{dx}\int_x^b f(t)\,dt$ | $-f(x)$ |
| $\displaystyle\frac{d}{dx}\int_a^{g(x)} f(t)\,dt$ | $f(g(x)) \cdot g'(x)$ |
| $\displaystyle\frac{d}{dx}\int_{h(x)}^{g(x)} f(t)\,dt$ | $f(g(x)) \cdot g'(x) - f(h(x)) \cdot h'(x)$ |
| $\displaystyle\frac{d}{dx}\int_a^{x} f(t,x)\,dt$（含参） | $f(x,x) + \displaystyle\int_a^x \frac{\partial f(t,x)}{\partial x}\,dt$ |

> ⚠️ **注意**：变限积分求导是考研高频考点，常与洛必达法则结合用于 $0/0$ 型极限！

---

> 📎 **关联文件**：[高数题型总览](/Math/calculus_overview) | [返回考研总览](/)


---

## 📝 例题精讲

> 以下例题从 [极限例题精讲](calculus_limit.md) 中分离，核心考察导数定义、可导性判定、高阶导数、参数方程求导。

### 例题：$0/0$ 型极限 · 导数定义法（1994 数三）

> **题目**（1994 数三 例17）：已知 $f'(x_0) = -1$，求极限 $\displaystyle\lim_{x\to 0}\frac{x}{f(x_0-2x)-f(x_0-x)}$

**思路分析**：

本题考察**导数定义求极限**，分子 $x\to 0$，分母 $f(x_0-2x)-f(x_0-x)\to 0$，为 $0/0$ 型未定式。核心是先求出分母差与 $x$ 比值的极限（即导数定义形式），再取倒数得到原极限。

---

**解法一：化为导数定义 + 取倒数**

先计算分母差与 $x$ 的比值：

$$
\begin{aligned}
&\lim_{x\to 0}\frac{f(x_0-2x)-f(x_0-x)}{x} \\[4pt]
=&\lim_{x\to 0}\frac{[f(x_0-2x)-f(x_0)]-[f(x_0-x)-f(x_0)]}{x} \\[4pt]
=&\lim_{x\to 0}\frac{f(x_0-2x)-f(x_0)}{x} - \lim_{x\to 0}\frac{f(x_0-x)-f(x_0)}{x}
\end{aligned}
$$

分别计算两个极限：

**第一项**：令 $t = -2x$，则 $x = -\dfrac{t}{2}$，$x\to 0$ 时 $t\to 0$

$$
\lim_{x\to 0}\frac{f(x_0-2x)-f(x_0)}{x}
= \lim_{t\to 0}\frac{f(x_0+t)-f(x_0)}{-t/2}
= -2\lim_{t\to 0}\frac{f(x_0+t)-f(x_0)}{t}
= -2f'(x_0) = -2\times(-1) = 2
$$

**第二项**：令 $t = -x$，则 $x = -t$，$x\to 0$ 时 $t\to 0$

$$
\lim_{x\to 0}\frac{f(x_0-x)-f(x_0)}{x}
= \lim_{t\to 0}\frac{f(x_0+t)-f(x_0)}{-t}
= -\lim_{t\to 0}\frac{f(x_0+t)-f(x_0)}{t}
= -f'(x_0) = -(-1) = 1
$$

因此 $\displaystyle\lim_{x\to 0}\frac{f(x_0-2x)-f(x_0-x)}{x} = 2 - 1 = 1$。

原极限取其倒数：

$$
\lim_{x\to 0}\frac{x}{f(x_0-2x)-f(x_0-x)}
= \frac{1}{\displaystyle\lim_{x\to 0}\frac{f(x_0-2x)-f(x_0-x)}{x}}
= \frac{1}{1} = 1
$$

> ✅ **答案：$1$**

---

**解法二：公式法（速算）**

由导数定义可得公式 $\displaystyle\lim_{x\to 0}\frac{f(x_0+\alpha x)-f(x_0+\beta x)}{x} = (\alpha-\beta)f'(x_0)$。

代入 $\alpha = -2$，$\beta = -1$，$f'(x_0) = -1$：

$$
\lim_{x\to 0}\frac{f(x_0-2x)-f(x_0-x)}{x} = [(-2)-(-1)]\times(-1) = 1
$$

原极限取倒数即得：

$$
\lim_{x\to 0}\frac{x}{f(x_0-2x)-f(x_0-x)} = \frac{1}{1} = 1
$$

> ✅ **答案：$1$**

---

> 💡 **启示与要点**：
> 1. **识别标志**：极限式中出现 $f(x_0+\alpha x)-f(x_0+\beta x)$，分母含 $x$ → **立即想到导数定义**，无需犹豫！
> 2. **分子为 $x$ 的处理技巧**：当极限分子为 $x$、分母为函数差时，先求分母差与 $x$ 比值（导数定义形式）的极限，再取倒数。
> 3. **导数定义的标准形式**：$f'(x_0) = \displaystyle\lim_{h\to 0}\frac{f(x_0+h)-f(x_0)}{h}$，核心是分子差与分母 $h$ 对应。
> 4. **拆分技巧**：当分母为 $f(x_0+\alpha x)-f(x_0+\beta x)$ 时，通过加减 $f(x_0)$ 拆成两项，每项都是导数定义的形式。
> 5. **核心公式**：$\displaystyle\frac{f(x_0+\alpha x)-f(x_0)}{x} = \alpha f'(x_0)$，$\alpha$ 可为负数（负号直接代入即可）。
> 6. 注意 $f'(x_0) = -1$ 为负数，代入时不要丢掉负号。

---


### 例题：导数定义判定可导性·含绝对值（2018 数一/二/三）

> **题目**（2018 例20）：下列函数中在 $x=0$ 处不可导的是（ ）
>
> A. $f(x)=|x|\sin|x|$
> B. $f(x)=|x|\sin\sqrt{|x|}$
> C. $f(x)=\cos|x|$
> D. $f(x)=\cos\sqrt{|x|}$

**思路分析**：

本题考察用**导数定义**判定可导性。核心套路分三步：

1. **先代入 $x=0$ 得 $f(0)$**——四个函数在 $0$ 处均有定义
2. **写出导数定义** $f'(0) = \displaystyle\lim_{x\to 0}\frac{f(x)-f(0)}{x}$
3. **用等价无穷小判断阶数**——若 $f(x)-f(0)$ 是 $x$ 的高阶无穷小 ⇒ 可导（导数为 $0$）；若恰为同阶，则需看左右是否相等

注意到各选项含 $|x|$，而 $\sin u \sim u$、$\cos u-1 \sim -\dfrac{u^2}{2}$（$u\to0$），可直接代入化简。

---

**解法：先代 $f(0)$ → 等价展开 → 判断**

**选项 A**：$f(x)=|x|\sin|x|$

$$
f(0) = 0,\qquad 
f'(0) = \lim_{x\to 0}\frac{|x|\sin|x|}{x}
$$

由 $\sin u \sim u$：

$$
|x|\sin|x| \sim |x|\cdot|x| = x^2 \quad(\text{高阶})
\quad\Rightarrow\quad \frac{|x|\sin|x|}{x} \sim x \to 0
$$

✅ **可导**（$f'(0)=0$）

---

**选项 B**：$f(x)=|x|\sin\sqrt{|x|}$

$$
f(0) = 0,\qquad 
f'(0) = \lim_{x\to 0}\frac{|x|\sin\sqrt{|x|}}{x}
$$

由 $\sin u \sim u$：

$$
|x|\sin\sqrt{|x|} \sim |x|\cdot\sqrt{|x|} = |x|^{3/2} \quad(\text{高阶})
\quad\Rightarrow\quad \frac{|x|^{3/2}}{x} = \frac{|x|^{3/2}}{x} \to 0
$$

✅ **可导**（$f'(0)=0$）

---

**选项 C**：$f(x)=\cos|x|$

$$
f(0) = 1,\qquad 
f'(0) = \lim_{x\to 0}\frac{\cos|x|-1}{x}
$$

$\cos|x|=\cos x$（$\cos$ 为偶函数），由 $\cos u-1 \sim -\dfrac{u^2}{2}$：

$$
\cos x-1 \sim -\frac{x^2}{2} \quad(\text{高阶})
\quad\Rightarrow\quad \frac{-\dfrac{x^2}{2}}{x} = -\frac{x}{2} \to 0
$$

✅ **可导**（$f'(0)=0$）

---

**选项 D**：$f(x)=\cos\sqrt{|x|}$ ← **不可导！**

$$
f(0) = 1,\qquad 
f'(0) = \lim_{x\to 0}\frac{\cos\sqrt{|x|}-1}{x}
$$

由 $\cos u-1 \sim -\dfrac{u^2}{2}$，其中 $u=\sqrt{|x|}$：

$$
\cos\sqrt{|x|}-1 \sim -\frac{(\sqrt{|x|})^2}{2} = -\frac{|x|}{2}
$$

代入导数定义：

$$
\frac{-\dfrac{|x|}{2}}{x} = -\frac{1}{2}\cdot\frac{|x|}{x}
= \begin{cases}
-\dfrac{1}{2}, & x\to 0^+ \\[6pt]
\ \ \dfrac{1}{2}, & x\to 0^-
\end{cases}
$$

左右导数不相等 ⇒ ❌ **不可导**

---

| 选项 | $f(0)$ | $f(x)-f(0)$ 的阶 | 结论 |
|:---:|:---:|:---:|:---:|
| A | $0$ | $\sim x^2$（高阶）| ✅ 可导 |
| B | $0$ | $\sim |x|^{3/2}$（高阶）| ✅ 可导 |
| C | $1$ | $\sim -\dfrac{x^2}{2}$（高阶）| ✅ 可导 |
| **D** | $1$ | $\sim -\dfrac{|x|}{2}$（**同阶**）| **❌ 不可导** |

> ✅ **答案：D**

---

> 💡 **启示与要点**：
> 1. **可导性判定标准流程**：用定义 $f'(x_0)=\displaystyle\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}$ 计算左右导数，看是否相等。
> 2. **含 $|x|$ 必分左右**：凡表达式含 $|x|$，在 $x=0$ 处讨论可导性时，**必须分左右极限**。
> 3. **关键等价代换**：$\cos u - 1 \sim -\dfrac{u^2}{2}$（$u\to 0$），本题中 $\sqrt{|x|}\to 0$ 时正好适用。
> 4. **选项 D 的本质**：$\cos\sqrt{|x|}$ 在 $x=0$ 处相当于 $\cos\sqrt{t}$ 在 $t=0$ 处关于 $t=|x|$ 的展开，左右两侧 $\sqrt{|x|}$ 的对称性被 $\cos$ 的二次项破坏，导致左右导数不相等。
> 5. **速记**：$|x|$ 的多项式函数乘 $\sin$ 往往可导（$\sin$ 一阶消去 $|x|/x$ 的符号），而 $\cos$ 复合 $\sqrt{|x|}$ 容易出问题（二次项展开后符号不对称）。

---


### 例题：高阶导数·莱布尼茨公式 / 麦克劳林展开（2015 数二）

> **题目**（2015 数二 例26）：函数 $f(x)=x^2\cdot 2^x$ 在 $x=0$ 处的 $n$ 阶导数 $f^{(n)}(0)=\underline{\qquad}$

**思路分析**：

求 $f^{(n)}(0)$ 有两种经典方法：
1. **莱布尼茨公式**：$f(x)=x^2\cdot 2^x$，其中 $x^2$ 求三阶以上导数为 $0$，只有两项贡献
2. **麦克劳林展开**：将 $2^x$ 展开为幂级数，与 $x^2$ 相乘后匹配 $x^n$ 项系数

---

**解法一：莱布尼茨公式（推荐）**

设 $u(x)=x^2$，$v(x)=2^x$，则 $f^{(n)}(x)=\displaystyle\sum_{k=0}^{n}C_n^k\,u^{(k)}(x)\,v^{(n-k)}(x)$。

各阶导数：
- $u(x)=x^2$，$u'(x)=2x$，$u''(x)=2$，$u^{(k)}(x)=0$（$k\ge 3$）
- $v^{(m)}(x)=2^x(\ln 2)^m$，$v^{(m)}(0)=(\ln 2)^m$

代入 $x=0$，只有 $k=2$ 项非零：

$$
\begin{aligned}
f^{(n)}(0) &= C_n^2\cdot u''(0)\cdot v^{(n-2)}(0) \\[4pt]
&= \frac{n(n-1)}{2}\times 2\times (\ln 2)^{\,n-2} \\[4pt]
&= n(n-1)(\ln 2)^{\,n-2}
\end{aligned}
$$

> ✅ **答案：$n(n-1)(\ln 2)^{\,n-2}$**

---

**解法二：麦克劳林展开（系数匹配法）**

将 $2^x = e^{x\ln 2}$ 展开为麦克劳林级数：

$$
2^x = \sum_{k=0}^{\infty} \frac{(\ln 2)^k}{k!}\,x^k
$$

则：

$$
f(x) = x^2\cdot 2^x = x^2\cdot\sum_{k=0}^{\infty} \frac{(\ln 2)^k}{k!}\,x^k
= \sum_{k=0}^{\infty} \frac{(\ln 2)^k}{k!}\,x^{k+2}
$$

$x^n$ 项对应 $k+2=n$，即 $k=n-2$（$n\ge 2$），系数为：

$$
\frac{(\ln 2)^{\,n-2}}{(n-2)!}
$$

由麦克劳林公式 $f(x)=\displaystyle\sum_{n=0}^{\infty}\frac{f^{(n)}(0)}{n!}x^n$，比较系数得：

$$
\frac{f^{(n)}(0)}{n!} = \frac{(\ln 2)^{\,n-2}}{(n-2)!}
\quad\Rightarrow\quad
f^{(n)}(0) = \frac{n!}{(n-2)!}\,(\ln 2)^{\,n-2} = n(n-1)(\ln 2)^{\,n-2}
$$

> ✅ **答案：$n(n-1)(\ln 2)^{\,n-2}$**

---

> 💡 **启示与要点**：
> 1. **莱布尼茨公式遇多项式**：当 $f(x)=$ 多项式 $\times$ 其他函数时，多项式求有限阶后为 $0$，莱布尼茨求和只需取很少几项，非常高效。
> 2. **麦克劳林展开法**：将函数展开为幂级数，$x^n$ 的系数为 $\dfrac{f^{(n)}(0)}{n!}$，适合 $f(x)$ 可展开为简单级数的情形。
> 3. **两种方法的联系**：本质上都是利用 $x^2$ 的"截断"特性——$x^2$ 三阶以上导数为 $0$（莱布尼茨），或展开后 $x^2$ 将级数指标平移 $2$（麦克劳林）。
> 4. **$n=0,1$ 的情况**：当 $n<2$ 时，$f^{(n)}(0)=0$，上述公式也成立（$n<2$ 时 $n(n-1)=0$）。

---


### 例题：参数方程求导·极坐标曲线切线（经典题）

> **题目**：已知对数螺线 $r = e^{\theta}$，求该螺线上对应点 $\left(r,\theta\right)=\left(e^{\pi/2},\dfrac{\pi}{2}\right)$ 处的切线在直角坐标系下的方程。

**思路分析**：

极坐标曲线求切线，先将极坐标化为**参数方程**：

$$
\begin{cases}
x = r\cos\theta = e^{\theta}\cos\theta \\[4pt]
y = r\sin\theta = e^{\theta}\sin\theta
\end{cases}
$$

然后按参数方程求导法求 $\dfrac{dy}{dx}$，再代入 $\theta = \dfrac{\pi}{2}$ 得切线斜率。

---

**解法**：

**第一步**：求 $\theta = \dfrac{\pi}{2}$ 处的直角坐标

$$
x_0 = e^{\pi/2}\cos\frac{\pi}{2} = e^{\pi/2}\times 0 = 0,\qquad
y_0 = e^{\pi/2}\sin\frac{\pi}{2} = e^{\pi/2}\times 1 = e^{\pi/2}
$$

即切点为 $(0,\;e^{\pi/2})$。

**第二步**：求切线斜率 $\dfrac{dy}{dx}$

$$
\frac{dx}{d\theta} = e^{\theta}\cos\theta - e^{\theta}\sin\theta = e^{\theta}(\cos\theta - \sin\theta)
$$

$$
\frac{dy}{d\theta} = e^{\theta}\sin\theta + e^{\theta}\cos\theta = e^{\theta}(\sin\theta + \cos\theta)
$$

由参数方程求导公式：

$$
\frac{dy}{dx} = \frac{dy/d\theta}{dx/d\theta}
= \frac{e^{\theta}(\sin\theta + \cos\theta)}{e^{\theta}(\cos\theta - \sin\theta)}
= \frac{\sin\theta + \cos\theta}{\cos\theta - \sin\theta}
$$

代入 $\theta = \dfrac{\pi}{2}$：

$$
\left.\frac{dy}{dx}\right|_{\theta=\frac{\pi}{2}}
= \frac{\sin\frac{\pi}{2} + \cos\frac{\pi}{2}}{\cos\frac{\pi}{2} - \sin\frac{\pi}{2}}
= \frac{1 + 0}{0 - 1} = -1
$$

**第三步**：写出切线方程

$$
y - e^{\pi/2} = -1\,(x - 0)
\quad\Longrightarrow\quad
\boxed{y = -x + e^{\pi/2}}
$$

> ✅ **答案：$y = -x + e^{\pi/2}$**

---

> 💡 **启示与要点**：
> 1. **极坐标求切线标准流程**：极坐标 $r=f(\theta)$ → 参数方程 $\begin{cases}x=f(\theta)\cos\theta\\ y=f(\theta)\sin\theta\end{cases}$ → $\dfrac{dy}{dx}=\dfrac{f'\sin\theta+f\cos\theta}{f'\cos\theta-f\sin\theta}$。
> 2. **对数螺线的优美性质**：$r=e^{\theta}$ 的 $\dfrac{dy}{dx}=\dfrac{\sin\theta+\cos\theta}{\cos\theta-\sin\theta}$，其切线与径矢的夹角恒为常数（等角螺线）。
> 3. 本题若 $\theta = \dfrac{\pi}{2}$，切点恰好在 $y$ 轴上（$x=0$），切线斜率为 $-1$，方程形式简洁。

---

