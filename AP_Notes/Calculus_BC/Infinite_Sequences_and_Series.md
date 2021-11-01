### Sequence
A sequence is a function whose domain is the non-negative integers. It can be expressed as a list of terms $\{a_n\} = \{a_1,a_2,a_3 ,...,a_n\}$.
A series $\sum{a_n}=\sum_{n=1}^{\infty}{a_n} = a_1+a_2+a_3+...+a_n$ is the sum of the terms of a sequence $\{a_n\}$. Associated with each series is a sequence of partial sums $\{s_n\}$, $s_1=a_1, s_2=a_1+a_2,s_3=a_1+a_2+a_3$, and in general, $s_n=a_1+a_2+a_3+...+a_n$.

Table of Series: ![[Table of Series Convergence Tests.jpg]]

### Types of Series
- **p-Series**
$$1+\frac{1}{2^p}+\frac{1}{3^p}+\frac{1}{4^p}+...+\frac{1}{n^p}=\sum_{n=1}^{\infty}\frac{1}{n^p}$$
==*Converges*== when $p>1$, ==*Diverges*== when $0<p\le1$.

- **Harmonic Series**
$$1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+...+\frac{1}{n}=\sum_{n=1}^{\infty}\frac{1}{n}$$The harmonic series is a p-series with $p=1$. The harmonic series *Diverges*.

- **Geometric Series**
A geometric series is a series of the form$$\sum_{n=1}^{\infty}ar^{n-1}$$where ==$a\ne0$==
==*Converges*== when ==$|r| < 1$==, otherwises ==*Diverges*==. The sum of the first $n$ terms of a geometric series is $$s_n=\frac{a(1-r)^n}{1-r}$$ The sum of the series $$\sum_{n=1}^{\infty}=\lim_{n\rightarrow\infty}s_n=\lim_{n\rightarrow\infty}\frac{a(1-r^n)}{1-r}=\frac{a}{1-r}$$

### Convergence Tests
- **Divergence Test**
Given a series $\sum_{n=1}^{\infty}$, if $\lim_{n\rightarrow\infty}a_n\ne0$, then the series ==*Diverges*==

- **Integral Test**
If $a_n=f(n)$where $f$ is a continuous, positive, decreasing function on $[c,\infty)$, then the series $\sum_{n=1}^{\infty}a_n$ is ==*convergent*== if and only if the improper integral $\int_{c}^{\infty}f(x)dx$ exists.

- **Ratio Test**
If $\sum_{n=1}^{\infty}a_n$ is a series with positive terms and $\lim_{n\rightarrow\infty}\frac{a_{n+1}}{a_n}<1$, then the series ==*converges*==. If the limit is greater than 1 or $\infty$, then the series ==*diverges*==. If the limit is 1, another test must be used.

- **Comparison Test**
Suppose $\sum_{n=1}^{\infty}b_n$ and $\sum_{n=1}^{\infty}b_n$ are series with non-negative terms, and $\sum_{n=1}^{\infty}b_n$ is known to *converge*. If a term-by-term comparison shows that for all $n$, $a_n\le b_n$, then $\sum_{n=1}^{\infty}a_n$ ==*converges*==.
if $\sum_{n=1}^{\infty}b_n$ *diverges*, and if for all $n$, $a_n \le b_n$, then $\sum_{n=1}^{\infty}a_n$ diverges.
	- In geometric series, it ==*converges*== for $r<1$ and ==*diverges*== for $r\ge1$
	- In p-series it ==*converges*== for $p>1$ and ==*diverges*== for $p\le1$

- **Limit Comparison Test**
if $\sum_{n=1}^{\infty}a_n$ and $\sum_{n=1}^{\infty}b_n$ are series with positive terms, and if $$\lim_{n\rightarrow\infty}\frac{a_n}{b_n}=L$$ where $0<l<\infty$, then either both series ==*converge*== of both ==*diverge*==.

- **Informal Principle**
Let a rational expression simpler and human readable $$\sum_{n=1}^{\infty}\frac{4n^3-n+1}{n^5+7n^2-6} \rightarrow \sum_{n=1}^{\infty}\frac{4n^3}{n^5}=4\sum_{n=1}^{\infty}\frac{1}{n^2}$$

### Alternating Series
- A series whose terms alternate between + and -
- It usually have one of two forms: $$\sum_{n=1}^{\infty}(-1)^na_n$$ or $$\sum_{n=1}^{\infty}(-1)^{n+1}a_n$$ with all $a_n > 0$
- It ==*converges*== if $a_1\ge a_2\ge a_3\ge ... \ge a_n$ and $\lim_{n\rightarrow\infty}a_n=0$

#### Error Bound
If an alternating series converges to the sum $S$, then $S$ lies between two consecutive partial sums of the series.
The absolute error $|S-s_n|$ is less than the next term $a_{n+1}$, and the sign of $S-s_n$ is the same as the coefficient of $a_{n+1}$.

#### Absolute and Conditional Convergence
1. $\sum_{n=1}^{\infty}a_n$ ==**converge absolutely**== if $\sum_{n=1}^{\infty}|a_n|$ converges. It also works in reverse direction.
2. Alternating series $\sum_{n=1}^{\infty}a_n$ is said to ==**converge conditionally**== if the series $\sum_{n=1}^{\infty}a_n$ converges but not absolutely.
3. If $\sum_{n=1}^{\infty}|a_n|$ diverges, then $\sum_{n=1}^{\infty}a_n$ may or may not converge.

#### Power Series
A power series is ~~*powerful series*~~ a series of the form $$\sum_{n=1}^{\infty}c_nx^n$$ where $c_1,c_2,c_3,...$ are constants and $x$ is a variable.
- **Radius and Interval of Convergence**
	- A power series centered at $x=a$ *converges* only for $x=a$, for all real values of x or for all x in some open interval ($a-R,a+R$), called interval of convergence.
	- The radius of convergence is $R$
	- If the series converges on ($a-R,a+R$), then it diverges if $x< a-R$ or $x<x-a+R$
		- The convergence or divergence must be investigated individually at $x=a-R$ and at $x=a+R$

### Taylor Series
A Taylor polynomial appraximates the value of a function $f(x)$ at the point $x=a$. If the function and all its derivatives exist at $x=a$, then on the interval of convergence, the Taylor series $$\sum^{\infty}_{n=0}\frac{f^{(n)}(a)}{n!}(x-a)^n$$converges to $f(x)$. When $x=0$, it is called MacLaurin series.
#### Common MacLaurin Series
$$e^x=\sum_{n=0}^{\infty}\frac{x^n}{n!}=1+x+\frac{x^2}{2!}+...+\frac{x^n}{n!}$$$$\sin x=\sum_{n=0}^{\infty}\frac{(-1)^nx^{2n+1}}{(2n+1)!}=x-\frac{x^3}{3!}+\frac{x^5}{5!}-...$$$$\cos x=\sum_{n=0}^{\infty}\frac{(-1)^{n}x^{2n}}{(2n)!}=1-\frac{x^2}{2!}+\frac{x^4}{4!}-...$$$$\tan x=\sum_{n=0}^{\infty}\frac{2^{2n}(2^{2n}-1)B_nx^{2n-1}}{(2n)!}=1+\frac{x^3}{3!}+\frac{2x^5}{15}... (For -\frac{\pi}{2}<x<\frac{\pi}{2})$$$$\cot x=\sum_{n=0}^{\infty}\frac{2^{2n}B_nx^{2n-1}}{(2n)!}=1+\frac{x^3}{3!}+\frac{2x^5}{15}...(For \space0<x<\pi)$$$$\ln(1+x)=x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+...(For-1<x\le1)$$**Binomial Series**$$(a+x)^n=a^n+na^{n-1}+\frac{n(n-1)}{2!}a^{n-2}x^2+\frac{n(n-1)(n-2)}{3!}a^{n-3}x^3+...$$For example:$$\frac{1}{1+x}=\sum_{n=0}^{\infty}(-1)^nx^n=1-x+x^2-...+(-1)x^n\space (For -1<x<1)$$$$\frac{1}{1-x}=\sum_{n=0}^{\infty}x^n=1+x+x^2+...+x^n\space (For -1<x<1)$$
#### Error Bounds
If the function $f(x)$ can be differentiated $n+1$ times on an interval containing $x_0$, and if $|f^{(n+1)}(x)|\le M$ for all x in that interval, then $$|R_n(x)|\le \frac{M}{(n+1)!}|x-x_0|^{n+1}$$for all x in the interval.
