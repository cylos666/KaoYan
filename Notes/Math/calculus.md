# 高等数学

## 泰勒展开基本函数前三项

泰勒展开式是将函数在某点附近用多项式逼近的方法。以下为常用基本函数在 $x=0$ 处的泰勒展开前三项（到 $x^2$ 项）：

### 1. 指数函数
$$e^x = 1 + x + \frac{x^2}{2!} + \cdots$$

### 2. 正弦函数
$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} + \cdots$$
前三项：$\sin x \approx x - \frac{x^3}{6} + O(x^5)$

### 3. 余弦函数
$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} + \cdots$$
前三项：$\cos x \approx 1 - \frac{x^2}{2} + \frac{x^4}{24}$

### 4. 自然对数函数
$$\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$
前三项：$\ln(1+x) \approx x - \frac{x^2}{2} + \frac{x^3}{3}$

### 5. 对数函数（变号）
$$\ln(1-x) = -x - \frac{x^2}{2} - \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$
前三项：$\ln(1-x) \approx -x - \frac{x^2}{2} - \frac{x^3}{3}$

### 6. 二项式函数（一般形式）
$$(1+x)^\alpha = 1 + \alpha x + \frac{\alpha(\alpha-1)}{2!}x^2 + \frac{\alpha(\alpha-1)(\alpha-2)}{3!}x^3 + \cdots$$
前三项：$(1+x)^\alpha \approx 1 + \alpha x + \frac{\alpha(\alpha-1)}{2}x^2$
> 常用特例：$\frac{1}{1+x} = (1+x)^{-1} = 1 - x + x^2 - x^3 + \cdots$

### 7. 几何级数（重要！）
$$\frac{1}{1-x} = 1 + x + x^2 + x^3 + \cdots$$
前三项：$\frac{1}{1-x} \approx 1 + x + x^2$

$$\frac{1}{1+x} = 1 - x + x^2 - x^3 + \cdots$$
前三项：$\frac{1}{1+x} \approx 1 - x + x^2$

### 8. 反正切函数
$$\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots$$
前三项：$\arctan x \approx x - \frac{x^3}{3} + O(x^5)$

### 9. 正切函数
$$\tan x = x + \frac{x^3}{3} + \frac{2x^5}{15} + \frac{17x^7}{315} + \cdots$$
前三项：$\tan x \approx x + \frac{x^3}{3} + O(x^5)$

### 10. 反正弦函数
$$\arcsin x = x + \frac{x^3}{6} + \frac{3x^5}{40} + \frac{5x^7}{112} + \cdots$$
前三项：$\arcsin x \approx x + \frac{x^3}{6} + O(x^5)$

---

## 考研数学·八大常用泰勒展开汇总（麦克劳林公式）

| 函数 | 展开式（前三项） | 通项规律 |
|:---:|:---|:---:|
| $e^x$ | $1 + x + \dfrac{x^2}{2!}$ | $\dfrac{x^n}{n!}$ |
| $\sin x$ | $x - \dfrac{x^3}{6} + \dfrac{x^5}{120}$ | $(-1)^k\dfrac{x^{2k+1}}{(2k+1)!}$ |
| $\cos x$ | $1 - \dfrac{x^2}{2} + \dfrac{x^4}{24}$ | $(-1)^k\dfrac{x^{2k}}{(2k)!}$ |
| $\ln(1+x)$ | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3}$ | $(-1)^{n-1}\dfrac{x^n}{n}$ |
| $\dfrac{1}{1-x}$ | $1 + x + x^2$ | $x^n$ |
| $\dfrac{1}{1+x}$ | $1 - x + x^2$ | $(-1)^n x^n$ |
| $(1+x)^\alpha$ | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2}x^2$ | $C_\alpha^n x^n$ |
| $\arctan x$ | $x - \dfrac{x^3}{3} + \dfrac{x^5}{5}$ | $(-1)^k\dfrac{x^{2k+1}}{2k+1}$ |

### 💡 常用等价无穷小（由泰勒展开推导）

当 $x \to 0$ 时：

- $e^x - 1 \sim x$
- $\sin x \sim x$
- $\tan x \sim x$
- $\arcsin x \sim x$
- $\arctan x \sim x$
- $\ln(1+x) \sim x$
- $(1+x)^\alpha - 1 \sim \alpha x$
- $1 - \cos x \sim \dfrac{1}{2}x^2$
- $x - \sin x \sim \dfrac{1}{6}x^3$
- $\tan x - x \sim \dfrac{1}{3}x^3$
- $x - \ln(1+x) \sim \dfrac{1}{2}x^2$
