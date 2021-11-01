Calculus Cheat Sheet
---
---
#### Common Derivatives
$$\frac{d}{dx}(\sin{x})=\cos{x}\space\space\space\space \frac{d}{dx}(\tan{x})=\sec^2{x}\space\space\space\space \frac{d}{dx}(\sec{x})=\sec{x} \tan{x}$$
$$\frac{d}{dx}(\cos{x})=-\sin{x}\space\space\space\space \frac{d}{dx}(\cot{x})=-\csc^2{x}\space\space\space\space \frac{d}{dx}(\csc{x})=-\csc{x}\cot{x}$$
$$\frac{d}{dx}(\sin^{-1}{x})=\frac{1}{\sqrt{1-x^2}}\space\space\space\space \frac{d}{dx}(\cos^{-1}{x})=-\frac{1}{\sqrt{1-x^2}}\space\space\space\space \frac{d}{dx}(\tan^{-1}{x})=\frac{1}{1+x^2}$$
$$\frac{d}{dx}(a^x)=a^x\ln{a}\space\space\space\space \frac{d}{dx}(e^x)=e^x \space\space\space\space\frac{d}{dx}(\ln{x})=\frac{1}{x}\space\space\space\space\frac{d}{dx}(\log_a(x))=\frac{1}{x\ln{a}}$$

#### Integrals and Common Integrals
>If you forget $+C$, you will get a $C$

$$\int_{a}^{b}f(x)dx=\lim_{n\rightarrow\infty}{\sum_{i=1}^{n}{f(x_i)}\Delta{x}}$$
$$\int{x^n}=\frac{x^{n+1}}{n+1}+C \space\space\space\space \int{\frac{1}{ax+b}}=\frac{1}{a}\ln{|ax+b|}+C \space\space\space\space \int{\ln{x}}=x\ln{x}-x+C \space\space\space\space$$
$$\int{e^x}=e^x+C \space\space\space\space \int{\cos{x}}=\sin{x}+C \space\space\space\space \int{\sin{x}}=-\cos{x}+C$$
$$\int{\tan{x}}=\ln{|\sec{x}|}+C \space\space\space\space \int{\sec{x}}=\ln{|\sec{x}+\tan{x}|}+C$$
$$\int{\frac{1}{a^2+x^2}}=\frac{1}{a}\tan^{-1}{(\frac{x}{a})}+C \space\space\space\space \int{\frac{1}{\sqrt{a^2-x^2}}}=\sin^{-1}{(\frac{x}{a})}+C$$

---
#### Taylor Series
$$\sum^{\infty}_{n=0}\frac{f^{(n)}(a)}{n!}(x-a)^n$$


#### Common MacLaurin Series
From $n=0$
$$e^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+...+\frac{x^n}{n!}$$$$\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+...+\frac{(-1)^nx^{2n+1}}{(2n+1)!}$$$$\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+...+\frac{(-1)^{n}x^{2n}}{(2n)!}$$$$\frac{1}{1+x}=1-x+x^2-...+(-1)^nx^n \space(For -1<x<1)$$$$\frac{1}{1-x}=1+x+x^2+...+x^n\space (For -1<x<1)$$From $n=1$$$\ln(1+x)=x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+...+\frac{(-1)^nx^n}{n}(For-1<x\le1)$$
