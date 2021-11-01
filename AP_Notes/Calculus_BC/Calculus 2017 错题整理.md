### Section A
- Question 5
![[2017 5.png]]
This question requires the knowledge of geometric series $\frac{a}{1-r}$, input the $\frac{-e}{\pi}$ as $r$, it become $$\frac{1}{1-\frac{-e}{\pi}}$$which equals $$\frac{\pi}{\pi + e}$$so the answer is ***C***

- Question 23
![[2017 23.png]]
For this question we need firstly write the beginning express of this sum:$$\sum_{n=1}^{\infty}\frac{x^{2n}}{n!}=x^2+\frac{x^4}{2!}+\frac{x^6}{3!}+...$$ The $f'(x)$ is simply derivative those things above:$$2x+2x^3+x^5+\frac{x^7}{3}...$$So the answer is ***D***

- Question 25
![[2017 25.png]]
In order to calculate the radius, we need to find the domain for $x$. We use $$\frac{1}{1-x}=1+x+x^2+x^3+x^4...$$to find $$\frac{1}{1+x}=\frac{1}{1-(-x)}=1-x+x^2-x^3+x^4...$$and substitute the $x^2$$$\frac{1}{1+x^2}=1-x^2+x^4-x^6+x^8...$$and the $2x$$$2x-2x^3+2x^5-2x^7+2x^9....$$Use $\sum$ to represent, we have $$\sum_{n=1}^{\infty}(-1)^{n-1}2x^{2n-1}$$ And now, we use the ratio test $2(n+1)-1=2n+1$ to find the domain of $x$:$$|\frac{2x^{2n+1}}{2x^{2n-1}}|=|x^2|<1$$