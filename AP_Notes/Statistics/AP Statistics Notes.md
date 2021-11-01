# AP Statistics Notes

Reviewing AP Stats as quick as possible after 11 months not touching it.
...
12 days later... DONE!

## Meta

Contents that are too intuitive or too useless are omitted from these notes.

Codes are written in python and are only for illustrating the concepts in statistics.

Do not assume everything is correct. I have probably made mistakes while taking notes but I will fix them as soon as I notice them.

Most of the graphs used in these notes come from the following sources:
- 5 Steps to a 5 AP Statistics by Corey Andreasen
- Khan Academy
- Google image

**Table of Content**

- [[#Meta|Meta]]
- [[#General|General]]
- [[#Calculator Notes|Calculator Notes]]
- [[#§1 One-Variable Data Analysis|§1 One-Variable Data Analysis]]
- [[#§2 Two-Variable Data Analysis|§2 Two-Variable Data Analysis]]
- [[#§3 Study Design|§3 Study Design]]
- [[#§4 Probability and Random Variable|§4 Probability and Random Variable]]
- [[#§5 Distributions|§5 Distributions]]
- [[#§6 Confidence Intervals|§6 Confidence Intervals]]
- [[#§7 Hypothesis Testing|§7 Hypothesis Testing]]
- [[#§8 Regression Inferences|§8 Regression Inferences]]
- [[#§9 Chi-Squared Tests|§9 Chi-Squared Tests]]

## General

- Types of statistics
	- **Descriptive statistics**, aka **exploratory data analysis**, only concerns about the data available
	- **Inferential statistics** uses available data to make prediction about the population
- Statistics vs parameters
	- **Parameters** describes the population
	- **Statistics** describes the sample
- Data types
	- Quantitative = number
	- Categorical = category
	- In between is possible
		- For example, grades can be quantitative and categorical
	- Discrete means data only take certain values
	- Continuous means smooth
- Histogram vs bar chart
	- They look similar, but
		- Histogram is for quantitative data
		- Bar chart is for categorical data
- Formality
	- Must specify what x and y refer to when writing responses
	- Do not write calculator notation on the exam. Just write what the calculator spits out
- Demonstrate that sampling distribution is normal before doing normal distribution math
- Do not talk about probability of true mean because the true mean is not random, so use "confidence" instead of "probability" when appropriate.
- Be sure to say that conditions for statistics are met before starting calculation
## Calculator Notes

This works on TI-nSpire CX but the principle applies on other models as well.

- `normCdf()` gives area between two bounds given mean and STD
- `normPdf()` gives the y value on a normal distribution graph
- `invNorm()` returns the x value given area to the left to the distribution
- `binomPdf()` returns the bionomial probability distribution for one $x$
- `binomCdf()` returns the probability distribution for a range of $x$
- `geomPdf()` does what it says
- `geomCdf()` does what it says
- The calculator has builtin t tests and z tests so look for them when needed.
- The calculator can also to chi-square figure out how to do that

## §1 One-Variable Data Analysis

- Graphical analysis
	- Things demonstrated with this data set
		![[Pasted image 20210902132323.png]]
	- Types of graph
		- Dotplot = each dot is a value and they are put on a numberline
			![[Pasted image 20210902132344.png]]
		- Stemplot, aka stem-and-leaf plot
			- The stem is the first digit and the second digit is the leave
			- Which digit to be used as the stem can be flexible
				![[Pasted image 20210902132355.png]]
			- The stems can even be split like this
				![[Pasted image 20210902132425.png]]
			- We can also put stem plots back to back like this
				![[Pasted image 20210902132450.png]]
		- Histogram
			- Different intervals produces different graph as illustrated here
				![[Pasted image 20210902132505.png]]
			- The ends of an interval are called boundaries
			- Usually the intervals include the bottom boundary but excludes the top boundary
		- Box-and-whiskers plot aka box plot
			- Basically, vertical lines represent Q1 Q2 and Q3 and the wiskers on the sides extend to last values that are not outliers
				![[Pasted image 20210902132513.png]]
			- Outliers will represented as dots outside of the whiskers 
				![[Pasted image 20210902132542.png]]
	- Shape
		- Symmetric = the graph is roughly symmetrical
		- Bell-shaped
		- Skewed
			- Skewed left = negatively skewed = has tail on left
			- Skewed right = positively skewed = has tail on right
		- Bimodal = has more than one peak
		- Uniform = almost flat
- Measuring center
	- Mean = `sum(list)`
	- Median
		```py
		length = len(list)
		if length % 2 ==0:
			return (list[(length/2)-0.5] + list[(length/2)+0.5]) / 2
		else:
			return list[length/2]
		```
	- Which one to use
		- If symmetric, shouldn't be  big problem which one
		- When strongly skewed, median may describe center better because it is a **resistant statistic** to extreme numbers.
	- Estimating center given graph
		- Median: find which $^{th}$ data should be used and find the interval that contains it
		- Mean: add values by pretending that the data is discrete at the midpoint of the intervals
- Measuring spread
	- Population Variance: $$\sigma_x=\sqrt{\frac{\sum^n_{i=1}(x_i-\mu)^2}{n}}$$from CPM text book
	- Sample Variance
		- Defined to be the average squared deviation of each data point from the mean
		- Formula $$s^{2}=\frac{1}{n-1} \sum\left(x_{i}-\bar{x}\right)^{2}$$
		- Note that it is divided by $n-1$ because knowing $n-1$ data points and $\bar{x}$ gives away the last data point
	- Sample Standard deviation
		- The sample standard deviation is the squareroot of the sample variance $$s = \sqrt{s^2} \text{ (Duh)}$$
		- Standard deviation is independent of
			- The mean
			- the sample size
	- Interquartile range (IQR)
		- Basically the technique used for finding mean is used to divide the data set into four quartiles
		- The interquartile is the range of the middle 50% of data points $$IQR = Q3 – Q1$$
	- Range
		- `return max(list) - min(list)`
- Outliers
	- There are different rules for identifying outliers
		- The **1.5(IQR) rule**
			- Outliers are those that lies outside of $Q1 – 1.5(IQR)$ or $Q3 + 1.5(IQR)$
		- Some also use 2 or 3 standard deviations away from mean rule
		- So watch out for which rule they ask for
- Percentile
	- Defined to be the point at which the percentile percent of the data are below the data point described by the percentile
- z-scores
	- A thing that describes how many standard deviations a data point is away from the mean
	- The formula, if not already obvious: $$z_{x i}=\frac{x_{j}-\bar{x}}{s}$$
	- In normal distribution, the z-score, together with a z-table, can help find the percentile.
- Normal distribution
	- A kind of beautiful, perfect, symmetric, bell-shaped distribution that occur naturally
	- The distrubution curve is given by this beast but never mind this isn't calculus class $$f(x)= {\frac{1}{\sigma\sqrt{2\pi}}}e^{- {\frac {1}{2}} (\frac {x-\mu}{\sigma})^2}$$
	- The **empirial rule**, aka the **68-95-99.7 rule**
		- Basically a breakdown of the distrubution within whole number standard deviations away from the mean as the pic illustrates	
			![[Pasted image 20210902132551.png]]
	- Standard normal distrubution
		- When dealing with theoretical distribution (viz. pure normal distribution), we use $\mu$ and $\sigma$ for mean and standard diavation to make the distinction.

## §2 Two-Variable Data Analysis

- **Two-variable**, aka **bivariate** data representation
	- Use scatterplot, which looks like
		![[Pasted image 20210902132559.png]]
	- In this type of data set, there's 
		- An **explanatory variable**, which goes onto the x axis
		- A **response variable**, which goes onto the y axis
		- Note that this isn't important in a correlation since there's no causality
- Correlation and regression
	- Refers to the relationship between the two data
	- This *does not* imply causality
	- The **correlation coefficient** $r$ measures the strength and direction of a correlation
		- This is calculated using the equation $$r=\frac{1}{n-1}\sum\left(\frac{x_{i}-\bar{x}}{s_{x}}\right)\left(\frac{y_{i}-\bar{y}}{s_{y}}\right)$$ or $$r=\frac{1}{n-1} \sum z_x z_y$$ basically, it's the average of the products of z scores (note that it divides by $n-1$ like sample standard deviation
			- When $r = 1$, there's a complete positive relationship
			- When $r = -1$, there's a complete negative relationship
			- When $r$ is in between, there is some relationship. The relationship gets stronger as they approach 1 or -1
			- The intuition is, z scores of different signs contribute to negative r whereas z scores of same signs contribute to positive r
			- ![[Pasted image 20210902132904.png|100]]
		- r can be used to calculate the regressing using this equation
			- ![[Pasted image 20210902132819.png|150]]
			- A calculator can also do this but make sure to know where to find the information. Usually the $b$ term is given by the `Coef` of `Constant` and the slope is given the `Coef` of the x variable.
		- r does not depend on the unit of measurement
		- r is not resistant to extreme values since mean is involved as illustrated here
			![[Pasted image 20210902133107.png]]
	- The **coefficient of determination** or **r-sq** is the square of r
		- It turns out that $r^2$ also equals to the percentage of error when predicting using least square regression compared to randomly gessing based on mean and STD.
		- Mathematically, 
			$$r^2 = \frac{SST-SSE}{SST}$$
			- In which **SST** is the **sum of squares total** by guessing y without knowing x
			- and **SSE** is the **sum of squared errors** after the using the regression to predict stuff
		- This percentage can also be interpreted that $r^2 \times 100\%$ of the variability in y can be explained by x.
	- To find a **line of best fit** aka a **least-squares regression line (LSRL)**, we want to find a line that minimises the sum of squared errors
		- Graphically, we try to minimise the area of these yellow squares
			![[Pasted image 20210902133320.png]]
		- A good practice is to not go beyond the data range when making predictions
			- Predictions within the data are called **interpolated predictions**; we can usually be confident about this type of prediction
			- Trying to predict outside of the data range is no good. Imagine predicting 100 years old person 6 metres tall using child growth data.
- **Residuals**
	- The residue for a prediction is the actual - estimated viz. $y - \hat{y}$
	- Graphically, it's that distance with sign
		![[Pasted image 20210902133335.png|100]]
	- In an ideal linear model, we expect the residuals to like the following, which can be checked with a residual plot like this
		![[Pasted image 20210902133414.png|400]]
		- randomly distributed
		- average to 0
		- normally distributed about 0
	- The **standard error of the residuals** $s$ estimates how much residuals vary
- Outliers
	- There's no clear guideline for two-variable data
	- A general rule is that outliers don't fall on the general data pattern and have large residue when the regression's done
- An **influential observation** is something influence the regression model strongly
- Non-linear models
	- When this happens, do it the AP Physics way

## §3 Study Design

- Types of studies
	- **Census:** sample the entire population of interest
		- This is sometimes impractical 
	- **Sample study:** use a properly selected sample to represent the population
		- Try to get a **representative sample** by reducing bias and being random
		- The list of all entities in the population that we sample from is called the **sampling frame**
- Probability Sampling methods
	- **Random sample**, by which samples are selected randomly from the population
		- A **simple random sample** is one in which every possible sample is equially probable
		- Note that simple random sample ⊂ random sample
			- Example: systematic sample is random but *not* simple random
	- **Systematic sample** is when the first is chosen randomly and the rest are chosen according to a pattern
		- Example: select the first sample randomly from first 10 entities and select every 10th person after that
	- **Stratified random sample** is when you do this
		![[Pasted image 20210902133456.png|300]]
	- **cluster sample** is when you do this
		![[Pasted image 20210902133508.png|300]]
- Non-random sampling techniques
	- **voluntary response sampling**
	- **convenience sampling**
	- **quota sampling**
		- Choosing sample based on demographic matching as illustrated here
			![[Pasted image 20210902133519.png|400]]
- Sampling biases
	- **Undercoverage bias:** some people are excluded from the sample
	- **Voluntary response bias:** only those who feel like respond responded
	- **Nonresponse bias:** some people choose to not respond
	- **Wording bias:** the wording influences the response
	- **Response bias:** the response is not truthful because either
		- They don't understand the question
		- They want to please the interviewer
		- The question sequence influence the response
- Experimental vs observational studies
	- **Experimental:** do experiment to find causual relationship
		- In a controlled experiment, there are these variables
			- Treatment variable that affects something
			- Response variable viz. the outcome
			- Some **confounding variables** aka **lurking variable** that also affect the experimental outcome but cannot be isolated from the treatment variable. This introduces experimental error
				- Researchers try to hold these constant using **statistical control**
		- Principles for experimental design
			- randomization: randomly assign subjects to treatment or control to equalize them
			- replication: do it on multiple subjects
			- control: minimize influence from confounding variables
		- Types of experiments
			- **Completely randomized**
			![[Pasted image 20210902141010.png|500]]
			![[Pasted image 20210902141036.png|500]]
				- Note that a **placebo** is often used for the control group's treatment
			- **Doubld-blind**
				- This is when neither the subjects nor the researchers know which group is receiving which treatment. All they know is that they are participating in a study
			- **Block design**
				1. Divid sujects into blocks according to some characteristic
				2. Do a completely randomised experiment for each block
				![[Pasted image 20210902141055.png]]
			- **Matched-pairs**
				- Method 1
					1. Randomly assigning people into treatment or control
					2. Swap treatment and control and repeat the experiment
				- Method 2 (according to another source)
					1. Measure the before and after treatment for every subject
					2. Compare the result
				- Another one: paired subjects (probably not on the exam)
				![[Pasted image 20210902141121.png]]
	- **Observational:** just observe if there's any correlation
		- **Retrospective:** look at data for a sample of people
		- **Prospective:** Follow the behaviors of a bunch of sampled individuals

## §4 Probability and Random Variable

- Definitions
	- **sample space** = the collection of disjoint chance outcomes
		- Example, two coin flips will have this sample space:
			- HH
			- TT
			- HT
			- TH
	- **disjoint** = **mutually exclusive** = outcomes cannot happen at the same time
		- Example: have 0, 1, 2 heads is disjoint because they cannot happen at the same time
- Frequencies in a 2D category table
	- Marginal frequencies: frequencies of looking at only one category viz. totals on the sides
	- Joint frequencies: frequencies of middle cells
- Logical operations (ironically, notes are not taken in logical sequence)
	- Use set operations
	- Use Venn diagrammes
	- A complement of an event is the space not included in that event
		- This is denoted by a $'$; for example the complement of event $A$ is $A'$
	- **Conditional probility** = probability of one thing given another another event is happening
	- A **tree diagram** can be a helpful way to approach logical problems
- Independent events
	- Viz. events that do not change the probability of another event happening
	- In logical notation, events are independent if $P(A|B) = P(A)$
	- If two events $A$ and $B$ are independent,
		- $P(A and B) = P(A)P(B)$
		- $P(A or B) = P(A) + P(B) - P(A)P(B)$
- Random variables
	- Types
		- discrete
		- conginuous
- Statistical calculations for discrete variable
	- The expected value is just the mean of the possible outcomes weighted by its probability $$\mu_{x}=\sum x \cdot P(x)$$
	- The variance is all the variance weighted by its probability $$\sigma_{X}^{2}=\sum\left(x-\mu_{x}\right)^{2} \cdot P(x)$$
	- The standard deviation is the equare root of the variance $$\sigma_{X}=\sqrt{\sum\left(x-\mu_{x}\right)^{2} \cdot P(x)}$$
- Transformation or combination of random variables
	- Use graphical intuition, we get
		- $μ_{X±Y} = μ_X ± μ_Y$
	- For some profound reason, if X and Y are independent, $\sigma_{X+Y}^{2}=\sigma_{X}^{2}+\sigma_{Y}^{2}$

## §5 Distributions

- **Bionomial distributions**
	- It's defined to be an experiment with
		- Fix number of trials $n$
		- Two possible outcomes for each trial (usually success and failture)
		- Same probablity of success $p$ for both trials
		- Independent trials
		- $X$ is the count of success in an experiment
		- The distribution $X$ in $n$ trials is the bionomial distribution
	- In sample bionomial, assume binomial random if the sample size less than 10% of population size
	- A shorthand notation for bionomial probability is $B(n, p, x)$ (in words, this refers to the probability of getting $x$ successes in $n$ trials given $p$ as probability
	- To calculate $B(n, p, x)$, we use this formula, $$^n C_x(p)^x(1-p)^{n-x}$$ which boils down to:
		- Find probability of having $x$ success
		- Multiply by the probability of having $n-x$ failures
		- Consider all different ways to choose the successes among all trials
	- The mean of $X$ is given by $$\mu_{X}=n p$$
	- The standard distribution of $X$ is given by $$\sigma_{x}=\sqrt{n p(1-p)}$$
- Normal approximation to binomial distributions
	- Sometimes binomial distributions can be approximately normal if:
		- Expected number of successes and number of failures are greater than 10
		- Viz. $np ≥ 10$ and $n(1 − p) ≥ 10$
		- This is because, if the probability graph is low on both sides, the boundaries (where there is all successes or failures) will not influence the distribution much by squishing it
	- When this is the case, we can use the mean and STD to make predictions on the distribution assuming that things are normal
- **Geometric distribution**
	- This is the distribution that results when
		- Two possible outcomes for each trial (usually success and failure)
		- Same probablity of success $p$ for both trials
		- Independent trials
		- $X$ is the number of trials needed to get first success
		- The distribution $X$ is the geometric distribution
	- The probability of first success landing at $X = n$ is given by, $$P(X = n) = (1 − p)^{n−1}p$$ which is essentially the probability of not getting a success until the $n^{\text{th}}$ trial
	- With some algebra we can calculate the expected wait time until first success, which turns out to be $$E(X) = \frac{1}{p}$$
	- A geometric distribution usually looks like this
	![[Pasted image 20210902141218.png|500]]
- **Sampling distribution**
	- The **sampling distribution of the sample mean** $\hat{x}$ is the distribution that we get when we find the mean of all possible samples of a certain type from the population
	- Assuming that the samples are independent (either by sampling with replacement or the sample is less than 10% of the population)
		- If the population is unknown, the theoretical mean and standard deviation for the sampling distribution is $$\mu_{\bar{x}}=\mu$$ and $$\sigma_{\bar{x}}=\frac{\sigma}{\sqrt{n}}$$ where $\mu$ and $\sigma$ are population mean and standard deviation
	- If no replacement take place, the exact STD of the sampling distribution is $$\sigma_{g}=\frac{\sigma}{\sqrt{n}} \sqrt{\frac{N-n}{N-1}}$$ ending square root thing is the **finite population correction factor**
- Shape expactation of sampling distribution of sample mean (**central limit theorem**)
	- When the sample size is small
		- If the population is normally distributed
			- The sampling distribution will be normal
		- If the population is not normal
			- The sampling distribution approximates the original shape
	- If sample size is large ($n>30$)
		- Normal sampling distribution no matter what
		- It gets more and more normal as sample size increases
		- The z procedure, though not regorous in this situation, works not bad with large $n$
- **Sampling distribution of a sample proportion**
	- Notation: we se $p$ for the population parameter and $\hat{p}$ as the statistic
	- The distribution of $\hat{p}$ will be described with $$\mu_{\hat{p}}=p$$ and $$\sigma_{\hat{p}}=\sqrt{\frac{p(1-p)}{n}}$$
	- Once again, the sampe becomes approximately normal when $n$ goes up
		- Additionally, when dealing with binomial, make sure that the number of successes and failures exceed 10.

## §6 Confidence Intervals

- The $z$ procedure
	- We use this when trying to estimate a proportion
	- When we try to use statistic to estimate a parameter, we need to provide a **confidence interval** around the **point estimate** produced by the statistic
		- The **confidence level** refers to the frequency that the confidence interval will capture the true parameter of interest upon repeated sampling
		- When taking a confidence level of, for example 95%, we are asking the following
			- What is the probability that $\hat{p}$ is within $2\sigma_\hat{p}$ (the central 95% normalCdf) of the actual $p$
			- When this is true, it is also true that there is 95% probability that $p$ is within $2\sigma_\hat{p}$ of $\hat{p}$
		- The trouble here, however, is that we do not know the $p$ to calculate $\sigma_\hat{p}$
			- To solve this, we use the standard error $SE_\hat{p}$ instead, which is given by $$SE_\hat{p} = \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
			- The mathematical formulation would then be $$\hat{p} \pm z^* \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
				- In $z^*$ is referred to as the **critical value**; it's the $z$ score that describes the confidence interval
		- The **margin of error** is how far you need to go from the point estimate to the endpoints of the confidence interval
			- This value increases as the confidence level increases because you need a larger interval to be more confident
	- Conditions to use this
		- Once again, the distribution of sample proportion can be assumed normal when expected successes and failures are both greater than 10
		- The sample is random
		- The sample should be independent so it shouldn't be larger than 10% of the population
- The $t$ procedure
	- We use this when trying to estimate a population mean
	- Considering the $z$ procedure in this case given by, $$\bar{x} \pm z^{*} \cdot \frac{s}{\sqrt{n}}$$ turns out that this is not a good way to estimate the real mean when we don't know the population STD, so mathematicians cam up with the $t$ procedure to be used with the sample STD
	- All it does is to map the $z$'s to a different $t$ to make the result accurate when applying this $$\bar{x} \pm t^{*} \cdot \frac{s}{\sqrt{n}}$$
	- To find the $t^*$, we need to know both our desired confidence level and the **degree of freedom (df)**, which can be calculated by $n-1$
	- Conditions to use this
		- Independence. Take no more than 10% of the population as sample
		- Normal. Either normal population or at least 30 samples
		- Random as always
- Confidence interval for differences between groups
	- Recall formulas to combine mean and STD
	- Use your brain and... it works alright (for proportions but not for means, because an extra adjustment is needed (but never mind it's close enough to get the work done))
- Selecting sample size
	- Usually, it costs to increase sample size, so researchers only want it large enough to get a reasonable maximum margin of error by solving this equation $$M \leq z^{*} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
	- However, we don't really know $\hat{p}$ since we havn't done the sampling, so we can either
		- Use $\hat{p}$ from previous studies
		- Use $\hat{p} = 0.5$ since it maximises $M$
	- For mean estimation, we don't know $t^*$ since we don't know $n$, so we just use $$M \leq z \cdot \frac{\sigma}{\sqrt{n}}$$

## §7 Hypothesis Testing

- The $p$ value is used as an indicator of statistical significance
	- Conceptually, the p-value tells the probability of getting by chance the measured statistic or anything even more extreme beyond that based on the null hypothesis
- Hypothesis
	- The **null hypothesis** is when nothing unusual is going on
	- We have to have statistically significant evidence to overthrow a null hypothesis, and we use the Greek letter $\alpha$ to denote a statistical significance
	- Basically, if the sample shows a that is not very probable to happen (to a certain extent), we say that the result is statistically insignificant, suggesting that there is something fishy going on.
- Hypothesis testing
	- When testing a hypothesis, we look for evidence that is against the hypothesis
	- The process goes like (use this to get full score)
		1. Set and state the null hypothesis that says nothing different is going on. Mathematically, the null hypothesis looks like $$H_0: μ1 − μ2 = 0$$
		2. Define and state an alternative hypothesis that tries to reject the null hypothesis. They can be either of the following $$H_A: μ1 − μ2 ≠ 0 \text{ (a two-sided alternative)}$$$$H_A: μ1 − μ2 > 0\text{ (a one-sided alternative)}$$$$H_A: μ1 − μ2 < 0\text{ (a one-sided alternative)}$$ Note that when using a one sided alternative, the null hypothesis can be written as the whole other side that the alternative tries to disprove
		3. Define a confidence interval $\alpha$
		4. Make sure that the conditions for making inferences are met, including
			- Larger than 10 successes and failures if dealing with $p$
			- If we can't find $p$ for the two sample pools, the best thing we can do is to dump the samples together and estimate $\hat{p}$ of the big pool, viz. $$\hat{p}=\frac{x_{1}+x_{2}}{n_{1}+n_{2}}=\frac{n_{1} \hat{p}_{1}+n_{2} \hat{p}_{2}}{n_{1}+n_{2}}$$
		5. Compare p value
			- Make sure to use the procedure appropriate for the problem
			- Make sure to consider if it's one or two sides
		6. Make a conclusion
			- The conclusion would be to either reject or fail to reject reject the null. It's *never* accept the null
	- Estimating the population proportion
		- To do this with a hypothesis test, we basically assume a $p_0$ and use it to calculate the standard error if the assumed $p$ is true
		- Difference between population proportions
			- The principle is the same
			- Once again, we dump two samples together to get the $\hat{p}$
- Errors and power
	- If we rejected an $H_0$ that we shouldn't reject, we call it a **type I error**
		- This happens at a probability of $\alpha$ (look at graph for intuition)
	- If we failed to reject an $H_0$ that we should reject, we call it a **type II error**
		- The probability of this happening is quite tricky to calculate
	- There is a trade off between making a type I and type II error
	- The probability of correctly rejecting an $H_0$ that should be rejected is called the **power** of the test. It can be demonstrated that this is equal to 1 - the probability of making a type II error as here shown
	![[Pasted image 20210902141324.png|400]]
	- The power of a test increases if
		- Sample size increases
		- Lower sample STD
		- Increase $\alpha$
		- Bigger difference in hypothesized value and the true value
- Difference between z and t procedure
	- When dealing with proportion, we kind of have an idea of how our sample statistic is going to be distributed so we can be safe with the z procedure
	- However, with population mean, we don't know the population STD so we will need to use t (well, we can still use z if we know the STD)
- Confidence interval can also be used to test a hypothesis because if the null hypothesis value is outside the confidence interval around the sample statistics with confidence level C, there is a 1 - C significance that the null hypothesis is not true (use graphic intuition)
- Comparing two population means
	- Same logic
	- Bit more complicated
	- Involves degree of freedom which can be found using `min(n1 - 1, n2 - 1)`
- When conditions for inference is not met according to what's explicitly stated in the question, we can
	- Make reasonable assumptions
- Matched pairs
	- When dealing with data from match pair, they are *not* independent
	- Which means that we just need to do a one-sample test on the differences between each matched data point

## §8 Regression Inferences

- Pourquoi
	- Recall simple linear regression from a while ago
		- Notice that we are doing this for the population
	- When we only have a sample available, we have to estimate the population regression line 
- Conditions for making inference
	- The values of the response variable are independent and normally distributed for each value of x
	- The STD is the same for each value of x
	- The data fit a linear trend
	- Example? Here
	![[Pasted image 20210902141348.png]]
- Notation
	- For the population, there is a true linearly relation given by the equation $\mu_y = \alpha +\beta x$ with standard deviation $\sigma$
	- The estimated equation would be given by $\hat{y} = a + b x$ with STD $s$
- Residual for inferred regression equation
	- Just like residual for least square regression, the residual for this can be calculated with $y_i - \hat{y}_i$
	- There is a standard error for the residual, which is given by this equation (why divided by $n - 2$ I cannot tell) $$s=\sqrt{\frac{S S_{\text {RSS }}}{n-2}}=\sqrt{\frac{\sum\left(y_{i}-\hat{y}_{i}\right)^{2}}{n-2}}$$ turns out that this is a predictor for $\sigma$
	- There is also a standard error for the slope of the regression line $s_b$ that can be calculated in some strange way
- Hypothesis testing for regression line
	- Our null hypothesis usually that $H_0: β = 0$
	- Our alternative hypothesis will thus be that the slope is not equal to 0 in some way (whatever the way)
	- Procedure
		- Use $t$ procedure
		- For some reason $df = n - 2$ (probably because this is a two variable situation)
- Constructing confidence interval for $\beta$
	- Use $n - 2$ as degree of freedom
	- Then follow the normal procedure:
		1. Find $t^*$ needed for the confidence level
		2. Find $b±t^*s_b$
	- Or consult a calculator
		- Example: in this output, the St Dev for Number is our $s_b$
		![[Pasted image 20210902142742.png]]

## §9 Chi-Squared Tests

- (This thing is written $\chi$ and pronounced /ˈkaɪ/)
- Pourquoi
	- So far we have been dealing with data with two outcomes (either success or failure) but not data that is categorical (viz. more than two outcomes)
	- Chi-Square will address that
- Example: if we have answer choices A, B, C, and D, and they are supposed to have equal probability
	- The null hypothesis is thus every choice has 0.25 probability
	- The alternative hypothesis is that the real proportion is not equal to 0.25
	- In this case, we use the Chi-square statistic to find out how extreme some value is in a sample
- How to do it
	- The degree of freedom for a chi-square scenario, now written $k$, is always $n-1$ because we can figure out the last one if everything else is known.
	1. Find sum of the square differences between the expected value and the actual value divided by the expected value as shown
	2. Look for the p value that correspond to that $\chi^2$ value
	![[Pasted image 20210902143147.png]]
	- (When reading the $p$ value from a table, we often get an interval for p since things are not exact)
- Conditions for making chi-square inferences
	- Random as always
	- Expected number of each outcome is greater than 5
	- Independent trials, so population ten times larger than sample size or sample with replacement
- Test for **homogeneity**
	- We do this to test how similar two groups are in terms of the distribution of outcomes
	- For example
		- $H_0$: there is no difference in subject preference between right handed and left handed people
		- $H_a$: there is a different
		1. Take a sample from right hand and left hand respectively
		2. Notice that if $H_0$ is true, the distribution in the total column will be the best estimate of the population distribution as shown here
		![[Pasted image 20210902143213.png|400]]
		1. Check conditions
		2. Calculate $\chi^2$
		![[Pasted image 20210902143446.png|400]]
		1. The degree of freedom is $(n_{\text{rows}} - 1)(n_{\text{columns} - 1})$. (in this case, indeed knowing two values allows you to know all data from all the totals)
		2. Find $p$ from chi-table
- Test for **association/independence**
	- The difference is, we only sample from one population but we measure two value from the same sample
	- The procedure
		- $H_0$: foot and hand length are independent
		- $H_a$: there is association
		1. Assume that the null hypothesis is true, calculate the expected value for each outcome
		2. Make sure conditions for inference are met
		3. Calculate $\chi^2$
			![[Pasted image 20210902143501.png|400]]
- Note on notations
	- Sometimes $r$ and $c$ are used to represent the number of rows and columns