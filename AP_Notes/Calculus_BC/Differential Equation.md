### Exponential Growth and Decay
---
#### Case I: Exponential Growth
Usually statement:
>A positive quantity y increases (or decreases) at a rate that at any time t is proportional to the amount present.

It follows that the quantity y satisfies $$\frac{dy}{dt}=ky\space_{(1)}$$where $k>0$ if y is increasing and $k<0$ if $y$ is decreasing. From $_{(1)}$ we know $$\frac{1}{y}dy=k\space dt$$$$\int\frac{1}{y}dy=\int k\space dt$$$$\ln{y}=kt+C$$ Then $$y=e^{kt+C}=Ce^{kt}$$which is the law of exponential change, it tells us that $C$ is the initial amount of $y$ (when $t=0$) 
```py
if k > 0:
	for i in range(time):
		y.increase()
elif k <0:
	for i in range(time):
		y.decrease()
```
The length of time required for a quantity that is decaying exponentially to be reduced by half is called its *half-life*.

#### Case II: Restricted Growth
The rate of change of $y$ may be proportional, not to the amount present but to a difference between that amount and a fixed constant. 
Two situations are to be distinguished: The rate of change is proportional to
- A fixed constant $A$ minus the amount of the quantity present: $$f'(t)=k[A-f(t)]$$
- The amount of the quantity present minus a fixed constant $A$: $$f'(t)=-k[f(t)-A]$$

Since both $f(t)$ is the amount at time $t$ and $k$ and $A$ are both positive. We can conclude that:
- $f(t)$ is increasing $$f(t)=A-ce^{-kt}$$
- $f(t)$ is decreasing $$f(t)=A+ce^{-kt}$$

For positive constant c

#### Case III: Logistic Growth
The rate of change of $f(t)$  (e.g. population) may be proportional both to the amount of the quantity and to the difference between a fixed constant $A$ and its amount. If $y=f(t)$, then $$y'=ky(A-y)$$ This equation is called the *logistic differential equation* it is used to model logistic growth. $$y=\frac{A}{1+ce^{-Akt}}$$
Which A is the capacity (or upper limit) of $f$ in this growth model.