# Probability
A **change event (random phenomenon)**, in this section we will use empirical method to decide the probabilities. We repeat the random process and record the result, then use the result to predict the future. 
The **probability of an event** is the predicted long-run event. In other word, if we repeat a random process many times, the predicted proportion of outcomes that are "success" is the probability of success.
The probability of an event must be 0 or 1:
- 0: definitely not happen
- 1: definitely will happen

**Outcome**: One of the possible results of a chance process. 
**Event**: A collection of outcomes or simple events.

# Sample Spaces and Events
A **sample space** is a **complete** list of **disjoint** outcomes or events.
- "Complete" = all possibilities listed
- "Disjoint/**mutually exclusive**" = no outcomes in common

Probability of an event is denoted as $P()$, for instance the probability of event E is $P(E)$, this is given by $$P(E)=\frac{\text{Number of outcomes in E}}{\text{Number of outcomes in the sample space}}$$

**Marginal frequencies**
**joint frequencies**
**relative frequency**
**marginal relative frequencies**
**joint relative frequencies**

# Probabilities of Combined Events
**P(A or B)**: A happen ***OR*** B happen ***OR*** both happen, denoted as $$P(A\cup B)$$
**P(A and B)**: A happen ***AND*** B happen (so must be both happen together)

## Some basic stuffs
**Addition/Sum rule**: $$P(A\cup B) = P(A)+P(B)-P(A\cap B)$$
**Complement of an event A**: denoted as $\bar{A}$ or $A^c$, also $$P(A^c)=1-P(A)$$
**Multiplication Rule**: $$P(A\cap B)=P(A)\cdot P(B|A)$$

# Conditional Probability
"The probability of A given B", which is symbolized by $P(A|B)$

# Independent Events
Event A and B are *independent* iff the knowledge of one having occurred does not change the probability of the other one. 
A and B are independent iff $$P(A|B)=P(A)\text{ or }P(B|A)=P(B)$$
If apply the multiplication rule:$$A\bot B \iff P(AB)=P(A)P(B)$$

# Random Variables
A **random variables $X$**: a numerical value assigned to an outcome of a random event. Common expression: $P(X=x)$, refers to the probability that the random variable $X$ takes on the particular value $x$.

## Discrete Random Variables
A **discrete random variables (DRV)** is a random variable with a countable number of outcomes.

## Continuous Random Variables
A **continuous random variables (CRV)** is a random variable that ~~is continuous~~ associated with one or more intervals on the number line. 
