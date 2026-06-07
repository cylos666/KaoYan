# 考研常用基本不等式

> 📌 **本章内容**：代数不等式、函数不等式、积分不等式、琴生不等式

---

## 一、代数不等式

| 不等式 | 公式 | 取等条件 |
|:---|:---|:---:|
| **基本不等式** | $a^2 + b^2 \ge 2ab$ | $a = b$ |
| **AM–GM（二元）** | $\dfrac{a+b}{2} \ge \sqrt{ab}\;(a,b\ge 0)$ | $a = b$ |
| **AM–GM（$n$ 元）** | $\dfrac{a_1 + a_2 + \cdots + a_n}{n} \ge \sqrt[n]{a_1a_2\cdots a_n}\;(a_i\ge 0)$ | $a_1 = a_2 = \cdots = a_n$ |
| **AM–GM 推广** | $\dfrac{a}{b} + \dfrac{b}{a} \ge 2\;(ab>0)$ | $a = b$ |
| **柯西–施瓦茨** | $(\sum a_i^2)(\sum b_i^2) \ge (\sum a_i b_i)^2$ | $\dfrac{a_1}{b_1} = \dfrac{a_2}{b_2} = \cdots$ |
| **三角不等式** | $\|a\| - \|b\|\le \|a \pm b\| \le \|a\| + \|b\|$ | 同号/异号时取等 |
| **排序不等式** | 顺序和 $\ge$ 乱序和 $\ge$ 逆序和 | — |
| **伯努利不等式** | $(1+x)^n \ge 1 + nx\;(x > -1,\;n\in\mathbb{N}^+)$ | $x = 0$ |
| **伯努利推广** | $(1+x)^\alpha \ge 1 + \alpha x\;(x > -1,\;\alpha>1\;\text{或}\;\alpha<0)$ | $x = 0$ |

---

## 二、函数不等式（考研高频！）

> 以下均在定义域内成立，常用于极限放缩、导数证明题。

| 不等式 | 示意图 |
|:---|:---:|
| $e^x \ge 1 + x\;(\forall x\in\mathbb{R})$ | $e^x$ 在 $(0,1)$ 处切线 |
| $\ln(1+x) \le x\;(x > -1)$ | $\ln(1+x)$ 在 $(0,0)$ 处切线 |
| $\dfrac{x}{1+x} < \ln(1+x) < x\;(x > 0)$ | 双边放缩 |
| $\sin x < x < \tan x\;(x > 0)$ | 单位圆中的三角函数线 |
| $\arctan x < x < \arcsin x\;(0 < x < 1)$ | 反三角函数放缩 |
| $\dfrac{1}{1+x} < \ln\!\left(1+\dfrac{1}{x}\right) < \dfrac{1}{x}\;(x > 0)$ | 积分放缩 |

---

## 三、积分不等式

| 不等式 | 公式 |
|:---|:---|
| **柯西–施瓦茨（积分型）** | $\displaystyle\left(\int_a^b f(x)g(x)\,dx\right)^2 \le \int_a^b f^2(x)\,dx \cdot \int_a^b g^2(x)\,dx$ |
| **积分保序性** | 若 $f(x) \le g(x)$ 则 $\displaystyle\int_a^b f(x)\,dx \le \int_a^b g(x)\,dx$ |
| **积分估值** | $m(b-a) \le \displaystyle\int_a^b f(x)\,dx \le M(b-a)$，其中 $m \le f(x) \le M$ |
| **积分中值定理** | $\displaystyle\int_a^b f(x)\,dx = f(\xi)(b-a),\;\xi\in[a,b]$ |

---

## 四、琴生不等式（Jensen）

若 $f(x)$ 为区间 $I$ 上的**凸函数**（$f''(x) \ge 0$），则对 $\forall x_i\in I$：

$$
f\!\left(\frac{x_1 + x_2 + \cdots + x_n}{n}\right) \le \frac{f(x_1) + f(x_2) + \cdots + f(x_n)}{n}
$$

若 $f$ 为**凹函数**（$f''(x) \le 0$），不等号反向。

> **考研常见凸函数**：$x^2$、$e^x$、$x\ln x$、$-\ln x$
>
> **考研常见凹函数**：$\sqrt{x}$、$\ln x$、$\sin x$（$[0,\pi]$）

---

> 📎 **关联文件**：[返回考研总览](/)
