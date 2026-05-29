# 高等数学

## 泰勒展开基本函数前三项

泰勒展开式是将函数在某点附近用多项式逼近的方法。以下为常用基本函数在 $x=0$ 处的泰勒展开前三项（到 $x^2$ 项）：

### 1. 指数函数

$$
e^x = 1 + x + \frac{x^2}{2!} + \cdots
$$

### 2. 正弦函数

$$
\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} + \cdots
$$

前三项： $\sin x \approx x - \frac{x^3}{6} + O(x^5)$

### 3. 余弦函数

$$
\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} + \cdots
$$

前三项： $\cos x \approx 1 - \frac{x^2}{2} + \frac{x^4}{24}$

### 4. 自然对数函数

$$
\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots
$$

前三项： $\ln(1+x) \approx x - \frac{x^2}{2} + \frac{x^3}{3}$

### 5. 对数函数（变号）

$$
\ln(1-x) = -x - \frac{x^2}{2} - \frac{x^3}{3} - \frac{x^4}{4} + \cdots
$$

前三项： $\ln(1-x) \approx -x - \frac{x^2}{2} - \frac{x^3}{3}$

### 6. 二项式函数（一般形式）

$$
(1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)}{2!}x^2 + \frac{\alpha(\alpha-1)(\alpha-2)}{3!}x^3 + \cdots
$$

前三项： $(1+x)^\alpha \approx 1 + \alpha x + \frac{\alpha(\alpha-1)}{2}x^2$

> 常用特例： $\frac{1}{1+x} = (1+x)^{-1} = 1 - x + x^2 - x^3 + \cdots$

### 7. 几何级数（重要！）

$$
\frac{1}{1-x} = 1 + x + x^2 + x^3 + \cdots
$$

前三项： $\frac{1}{1-x} \approx 1 + x + x^2$

$$
\frac{1}{1+x} = 1 - x + x^2 - x^3 + \cdots
$$

前三项： $\frac{1}{1+x} \approx 1 - x + x^2$

### 8. 反正切函数

$$
\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots
$$

前三项： $\arctan x \approx x - \frac{x^3}{3} + O(x^5)$

### 9. 正切函数

$$
\tan x = x + \frac{x^3}{3} + \frac{2x^5}{15} + \frac{17x^7}{315} + \cdots
$$

前三项： $\tan x \approx x + \frac{x^3}{3} + O(x^5)$

### 10. 反正弦函数

$$
\arcsin x = x + \frac{x^3}{6} + \frac{3x^5}{40} + \frac{5x^7}{112} + \cdots
$$

前三项： $\arcsin x \approx x + \frac{x^3}{6} + O(x^5)$

---

## 考研数学·八大常用泰勒展开汇总（麦克劳林公式）

| 函数 | 展开式（前三项） | 通项规律 |
|:---:|:---|:---:|
| $e^x$ | $1 + x + \frac{x^2}{2!}$ | $\frac{x^n}{n!}$ |
| $\sin x$ | $x - \frac{x^3}{6} + \frac{x^5}{120}$ | $(-1)^k\frac{x^{2k+1}}{(2k+1)!}$ |
| $\cos x$ | $1 - \frac{x^2}{2} + \frac{x^4}{24}$ | $(-1)^k\frac{x^{2k}}{(2k)!}$ |
| $\ln(1+x)$ | $x - \frac{x^2}{2} + \frac{x^3}{3}$ | $(-1)^{n-1}\frac{x^n}{n}$ |
| $\frac{1}{1-x}$ | $1 + x + x^2$ | $x^n$ |
| $\frac{1}{1+x}$ | $1 - x + x^2$ | $(-1)^n x^n$ |
| $(1+x)^\alpha$ | $1 + \alpha x + \frac{\alpha(\alpha-1)}{2}x^2$ | $C_\alpha^n x^n$ |
| $\arctan x$ | $x - \frac{x^3}{3} + \frac{x^5}{5}$ | $(-1)^k\frac{x^{2k+1}}{2k+1}$ |

### 💡 常用等价无穷小（由泰勒展开推导）

当 $x \to 0$ 时：

- $e^x - 1 \sim x$
- $\sin x \sim x$
- $\tan x \sim x$
- $\arcsin x \sim x$
- $\arctan x \sim x$
- $\ln(1+x) \sim x$
- $(1+x)^\alpha - 1 \sim \alpha x$
- $1 - \cos x \sim \frac{1}{2}x^2$
- $x - \sin x \sim \frac{1}{6}x^3$
- $\tan x - x \sim \frac{1}{3}x^3$
- $x - \ln(1+x) \sim \frac{1}{2}x^2$

---

## 考研高数·题型分类总结

### 一、极限与连续

| 题型 | 核心方法 |
|:---|:---|
| **$0/0$ 型极限** | 等价无穷小代换、洛必达、泰勒展开 |
| **$\infty/\infty$ 型极限** | 洛必达、抓大头、分子分母同除最高次 |
| **$1^\infty$ 型极限** | 重要极限 $\lim(1+x)^{1/x}=e$，取对数 |
| **$\infty-\infty$ 型极限** | 通分、有理化、提公因式 |
| **$0\cdot\infty$ 型极限** | 化为 $0/0$ 或 $\infty/\infty$ |
| **无穷小比阶** | 泰勒展开到同阶 |
| **数列极限** | 单调有界准则、夹逼准则、定积分定义 |
| **无穷大 × 非零周期函数** | 无界但不为无穷大 |
| **复合函数反推内层极限** | 外层单调+内层有界→内层极限存在 |
| **连续与间断点** | 左右极限判定间断类型 |

### 二、一元函数微分学

| 题型 | 核心方法 |
|:---|:---|
| **导数定义求极限** | $f'(x_0)=\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}$ |
| **隐函数求导** | 两边同时对 $x$ 求导，解出 $y'$ |
| **参数方程求导** | $\frac{dy}{dx}=\frac{y'(t)}{x'(t)}$ |
| **高阶导数** | 莱布尼茨公式、数学归纳法 |
| **中值定理证明** | 罗尔定理、拉格朗日、柯西、泰勒 |
| **单调性与极值** | 一阶导数判单调，二阶导数判极值 |
| **凹凸性与拐点** | 二阶导数符号判断 |
| **渐近线** | 水平/垂直/斜渐近线 |
| **方程根的个数** | 零点定理 + 单调性 |

### 三、一元函数积分学

| 题型 | 核心方法 |
|:---|:---|
| **不定积分计算** | 凑微分、换元法、分部积分 |
| **定积分计算** | 牛顿-莱布尼茨、对称区间奇偶性 |
| **反常积分敛散性** | 比较判别法、极限判别法 |
| **定积分应用** | 面积、体积（旋转体）、弧长 |
| **变限积分求导** | $\frac{d}{dx}\int_{a(x)}^{b(x)}f(t)dt$ |
| **积分等式/不等式** | 积分中值定理、放缩法 |

### 四、多元函数微分学

| 题型 | 核心方法 |
|:---|:---|
| **偏导数与全微分** | 链式法则、全微分形式不变性 |
| **隐函数求偏导** | 公式法 $z_x=-\frac{F_x}{F_z}$ |
| **无条件极值** | $A=f_{xx}, B=f_{xy}, C=f_{yy}$，$AC-B^2$ 判别 |
| **条件极值** | 拉格朗日乘数法 |

### 五、多元函数积分学

| 题型 | 核心方法 |
|:---|:---|
| **二重积分计算** | 直角坐标/极坐标、交换积分次序 |
| **三重积分计算** | 直角/柱面/球面坐标 |
| **曲线积分** | 格林公式、与路径无关条件 |
| **曲面积分** | 高斯公式 |

### 六、微分方程

| 题型 | 核心方法 |
|:---|:---|
| **一阶线性** | 通解公式 $y=e^{-\int Pdx}(\int Qe^{\int Pdx}dx+C)$ |
| **可分离变量** | 分离后两边积分 |
| **二阶常系数齐次** | 特征方程 $r^2+pr+q=0$ |
| **二阶常系数非齐次** | 待定系数法 |

### 七、无穷级数（数一/数三）

| 题型 | 核心方法 |
|:---|:---|
| **常数项级数敛散性** | 比较/比值/根值/积分判别法 |
| **幂级数收敛域** | 收敛半径 $R=\lim \lvert a_n/a_{n+1} \rvert$ |
| **幂级数求和** | 逐项求导/积分、已知展开式 |
| **函数展开为幂级数** | 泰勒展开 |

---

## 洛必达法则失效的振荡函数专题

> **核心要点**：洛必达法则要求求导后极限存在（或为 $\infty$）。当导数中出现振荡项（如 $\sin\frac{1}{x}$、$\cos x$ 等）且极限不存在时，**洛必达法则失效**。此时需改用等价无穷小、夹逼准则或拆分法。

### 类型一：$x \to 0$ 时 $\sin\frac{1}{x}$ 型振荡

#### 典例 1：$\displaystyle \lim_{x \to 0} \frac{x^2 \sin\frac{1}{x}}{\sin x}$

**【洛必达 × 失效】** 分子求导：$2x\sin\frac{1}{x} - \cos\frac{1}{x}$，其中 $\cos\frac{1}{x}$ 在 $x\to0$ 时振荡无极限，洛必达不能用。

**正确解法**（等价无穷小）：

$$
\lim_{x\to0} \frac{x^2 \sin\frac{1}{x}}{\sin x}
= \lim_{x\to0} \frac{x^2 \sin\frac{1}{x}}{x}
= \lim_{x\to0} x \sin\frac{1}{x} = 0
$$

> ✅ **答案：$0$**

---

#### 典例 2：$\displaystyle \lim_{x \to 0} \frac{x \sin\frac{1}{x}}{\sin x}$

**【洛必达 × 失效】** 分子求导得 $\sin\frac{1}{x} - \frac{1}{x}\cos\frac{1}{x}$，振荡且发散，洛必达失效。

**正确解法**（等价无穷小）：

$$
\lim_{x\to0} \frac{x \sin\frac{1}{x}}{\sin x}
= \lim_{x\to0} \frac{x \sin\frac{1}{x}}{x}
= \lim_{x\to0} \sin\frac{1}{x} \quad\text{不存在}
$$

> ✅ **结论：极限不存在（振荡）**

---

#### 典例 3：$\displaystyle \lim_{x \to 0} \frac{x^3 \sin\frac{1}{x}}{x - \sin x}$

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

### 类型二：$x \to \infty$ 时 $\sin x$、$\cos x$ 型振荡

#### 典例 4：$\displaystyle \lim_{x \to \infty} \frac{x + \sin x}{x}$

**【洛必达 × 失效】** 洛必达得 $\displaystyle \lim_{x\to\infty} \frac{1+\cos x}{1}$，$\cos x$ 在无穷远处振荡无极限，洛必达失效。

**正确解法**（拆分法）：

$$
\lim_{x\to\infty} \frac{x + \sin x}{x}
= \lim_{x\to\infty} \left(1 + \frac{\sin x}{x}\right)
= 1 + 0 = 1
$$

> ✅ **答案：$1$**

---

#### 典例 5：$\displaystyle \lim_{x \to \infty} \frac{x - \sin x}{x + \sin x}$

**【洛必达 × 失效】** 洛必达后出现 $\frac{1-\cos x}{1+\cos x}$，$\cos x$ 振荡，极限不存在，洛必达失效。

**正确解法**（同除 $x$）：

$$
\lim_{x\to\infty} \frac{x - \sin x}{x + \sin x}
= \lim_{x\to\infty} \frac{1 - \frac{\sin x}{x}}{1 + \frac{\sin x}{x}}
= \frac{1 - 0}{1 + 0} = 1
$$

> ✅ **答案：$1$**

---

#### 典例 6：$\displaystyle \lim_{x \to \infty} \frac{x + \sin x}{x - \cos x}$

**【洛必达 × 失效】** 求导后出现 $\frac{1+\cos x}{1+\sin x}$，分子分母均振荡，极限不存在，洛必达失效。

**正确解法**（同除 $x$）：

$$
\lim_{x\to\infty} \frac{x + \sin x}{x - \cos x}
= \lim_{x\to\infty} \frac{1 + \frac{\sin x}{x}}{1 - \frac{\cos x}{x}}
= \frac{1 + 0}{1 - 0} = 1
$$

> ✅ **答案：$1$**

---

### 类型三：$x \to \infty$ 时 $\sin x^2$、$x\sin x$ 等混合振荡

#### 典例 7：$\displaystyle \lim_{x \to \infty} \frac{x^2 + \sin x}{x^2 + \cos x}$

**【洛必达 × 失效】** 求导得 $\frac{2x + \cos x}{2x - \sin x}$，再次求导得 $\frac{2 - \sin x}{2 - \cos x}$，分子分母均振荡，洛必达彻底失效。

**正确解法**（同除 $x^2$）：

$$
\lim_{x\to\infty} \frac{1 + \frac{\sin x}{x^2}}{1 + \frac{\cos x}{x^2}}
= \frac{1 + 0}{1 + 0} = 1
$$

> ✅ **答案：$1$**

---

### 💡 洛必达失效判定与应对策略

| 情形 | 特征 | 失效原因 | 应对策略 |
|:---|:---|:---|:---|
| **$x \to 0$，含 $\sin\frac{1}{x}$** | 分子/分母出现 $\sin\frac{1}{x}$、$\cos\frac{1}{x}$ | 求导后 $\cos\frac{1}{x}$ 振荡无极限 | 等价无穷小代换，消去振荡因子 |
| **$x \to \infty$，含 $\sin x$** | 分子/分母含 $\sin x$、$\cos x$ | 求导后 $\sin x$、$\cos x$ 振荡无极限 | 同除最高次幂，夹逼准则 |
| **可导但导数振荡** | $f(x)=x^2\sin\frac{1}{x}$ 类函数 | $f'(x)$ 在 $x=0$ 附近无极限 | 用定义或等价替换 |
| **分子分母均振荡** | 如 $\frac{1+\cos x}{1+\sin x}$ | 分子分母同时振荡，极限不存在 | 拆分或同除最高次 |

> **记忆口诀**：见到 $\sin\frac{1}{x}$ 洛必达先别急，等价代换是第一；见到 $\sin x$ 跑无穷，同除最高最轻松。

---

## 例题精讲

### 例题1：无穷小比阶 + 泰勒展开

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

### 例题2：$0/0$ 型极限 · 三步法

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

### 例题3：$1^\infty$ 型极限 · 重要极限法

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

### 例题4：数列极限 · 定积分定义

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

### 例题5：数列收敛的 ε-N 定义辨析

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

## 知识卡片：复合函数极限反推内层极限

> **定理**：设 $\displaystyle\lim_{x \to x_0} f(g(x)) = A$，且满足：
>
> 1. $f(u)$ **严格单调**（在 $u = \lim g(x)$ 的邻域内）
> 2. $g(x)$ **有界**
>
> 则 $\displaystyle\lim_{x \to x_0} g(x)$ 存在，且 $\lim g(x) = f^{-1}(A)$。

**直观理解**：

- $g(x)$ 有界 → 必有收敛子列（Bolzano-Weierstrass）
- 若 $g(x)$ 有两个不同极限点 $\alpha \neq \beta$，则 $f(g(x))$ 会趋向 $f(\alpha)$ 和 $f(\beta)$
- 但 $f$ 严格单调 ⇒ $f(\alpha) \neq f(\beta)$，与 $f(g(x))$ 有唯一极限 $A$ 矛盾
- 因此 $g(x)$ 只能有唯一极限点 → 极限存在

**考研常用场景**：已知 $\lim e^{g(x)}$、$\lim \arctan g(x)$ 等复合极限存在且 $g(x)$ 有界，反推 $\lim g(x)$。

---

### 例题6：复合函数反推内层极限

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

### 例题7：单调性判定·复合函数反推（2022 数一/二真题）

> **题目**（例15·2022 数一、二）：已知数列 $\{x_n\}$，其中 $-\dfrac{\pi}{2} \leq x_n \leq \dfrac{\pi}{2}$，则（ ）
>
> A. 当 $\displaystyle\lim_{n\to\infty}\cos(\sin x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}x_n$ 存在
>
> B. 当 $\displaystyle\lim_{n\to\infty}\sin(\cos x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}x_n$ 存在
>
> C. 当 $\displaystyle\lim_{n\to\infty}\cos(\sin x_n)$ 存在时，$\displaystyle\lim_{n\to\infty}\sin x_n$ 存在，但 $\displaystyle\lim_{n\to\infty}x_n$ 不一定存在
>
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

## 知识卡片：无穷大 × 非零周期函数

**结论**：设 $f(x)$ 为**非零周期函数**（如 $\sin x$、$\cos x$），$g(x) \to \infty$（$x \to x_0$），则：

$$
f(x) \cdot g(x) \quad\text{是}\quad \text{【无界但不为无穷大】}
$$

**为什么不是无穷大？**

无穷大的定义：$\forall M > 0$，$\exists \delta > 0$，当 $0 < |x-x_0| < \delta$ 时，$|h(x)| > M$。

但 $f(x) \cdot g(x)$ 不满足此定义——因为 $f(x)$ 周期性振荡，会**反复穿过零点**：

- 当周期函数取 $\pm 1$ 时：$|f \cdot g| = |g| \to \infty$（可以任意大 → **无界**）
- 当周期函数取 $0$ 时：$f \cdot g = 0$（无法保证始终大于任意 $M$ → **不是无穷大**）

**判定口诀**：

$$
\text{无穷大} \times \text{非零周期函数} = \text{无界} \neq \text{无穷大}
$$

**常见题型**：判断 $\dfrac{1}{x^k}\sin\dfrac{1}{x}$、$x\sin x$（$x\to\infty$）等的极限性质。

---

### 例题8：无穷大 × 周期函数·无界但不为无穷大（1993 数三真题）

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

### 例题9：$1^\infty$ 型极限·公式法速解（2022 数二/数三真题）

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
> - 与例题3对比：都是 $1^\infty$ 型，但本题用公式法更快

---

### 例题10：$1^\infty$ 型·数列极限·几何平均（经典题）

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
