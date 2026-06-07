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
