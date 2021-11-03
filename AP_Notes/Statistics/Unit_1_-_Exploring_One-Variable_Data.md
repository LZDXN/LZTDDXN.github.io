SOCS Vocab and Context Guide
---

## S: Shape
**Skewed or Symmetric?**
- Symmetric Example:
![[Pasted image 20210908110106.png|200]] ![[Pasted image 20210908110155.png|200]]
$\color{red}\text{Both distribution}$ of women's SSHA Score are $\color{red}\text{symmetric}$, which means that $\color{red}\text{there is a similar amount}$ of scores $\color{red}\text{above and below the middle } 50\%$.
- Skewed Example:
![[Pasted image 20210908110125.png|200]] ![[Pasted image 20210908110208.png|200]]
$\color{red}\text{The distribution of }$the words used in Shakespeare's letter are words $\color{red}\text{from 2 to 6}$ letters  $\color{red}\text{with fewer longer words up}$ to 12 letters.

## O: Outliers
- Are there any ==apparent outlier==? (1.5 IQR)
- There are no apparent outliers in the word distribution.

## C: Center
- Median - About half above/below
$\color{red}\text{The median length}$ of the words is 4 letters. $\color{red}\text{About half of}$ the words used in the plays are $\color{red}\text{shorter than 4}$ letters and $\color{red}\text{half of the words are above than 4}$ letters.

## S: Spread
- Range
- IQR
The words $\color{red}\text{range}$ from 1 letters to 12 letters. $\color{red}\text{Calculating the interquartile range (IQR), the middle }50\%$ of the words $\color{red}\text{range}$ from 3 to 6 letters. 
- When **large** number is added in the data set:
	- Mean $\to$ Increase
	- Median $\to$ Not substantially change
		The $\color{red}\text{mean}$ would $\color{red}\text{increase}$ for the  $\color{red}\text{larger data set}$, since it is **affected by outliers**. However, the  $\color{blue}\text{median}$ would $\color{blue}\text{not substantially change}$ since it is $\color{blue}\text{resistant to outliers}$. 
		\* Median may shift ever so slightly, since the number of samples in data set changes. 


****

- **statistic** ::: A numerical fact or calculation that is formed from a sample of data.
- **census** ::: When information from the entire population is available. （人口普查）
- **parameter** ::: A numerical fact or calculation that is formed from a census
- **bias** ::: systematically favoring certain outcomes
- **variation** ::: differences among and within sets of data, making comparisons difficult. 


## Displays of Categorical Data
- **bar graph**: Is used when data has mutually exclusive categories that typically have no numerical order
![[Pasted image 20210908104737.png|200]]
- **circle graph**: Is used when data has mutually exclusive categories that typically have no numerical order,  shows percentages of data.
![[Pasted image 20210908104859.png|200]]
- **two-way table**: Is used to show overlap and relationships between variables. ==Strictly== limited to two variables, each variable may have $\ge$ two response categories.
![[Pasted image 20210908105045.png|200]]
- **Venn diagram**: Is used to show frequencies, relationships, and overlap. It is not limited to two variables but limited to two responses (usually boolean question)
![[Pasted image 20210908105220.png|200]]

## Displays of Quantitative Data
- **dot plot**: A way of displaying data that has an order and can be placed on a number line.
![[Pasted image 20210908105312.png|200]]
- **histogram**: Similar to dot plot except that each bear represents data in an interval of numbers. (e.g. time)
![[Pasted image 20210908105404.png|200]]
- **stem-and-leaf-plot**: Shows the individual values from a set of data and how the values are distributed.
![[Pasted image 20210908105526.png|200]]
- **scatterplot**: Displays paired data. Each data pair is represented by a point on a two dimensional graph. 
![[Pasted image 20210908105602.png|200]]




# Notes translated for HUMAN

****

- Graphical analysis
	- Things demonstrated with this data set
		![[Pasted image 20210902132323.png]]
	- Types of graph
		- Dot plot = each dot is a value and they are put on a number line
			![[Pasted image 20210902132344.png|400]]
		- Stem plot, a.k.a. stem-and-leaf plot
			- The stem is the first digit and the second digit is the leave
			- Which digit to be used as the stem can be flexible
				![[Pasted image 20210902132355.png|300]]
			- The stems can even be split like this
				![[Pasted image 20210902132425.png|300]]
			- We can also put stem plots back to back like this
				![[Pasted image 20210902132450.png|400]]
		- Histogram
			- Different intervals produces different graph as illustrated here
				![[Pasted image 20210902132505.png|350]]
			- The ends of an interval are called boundaries
			- Usually the intervals include the bottom boundary but excludes the top boundary
		- Box-and-whiskers plot a.k.a. box plot
			- Basically, vertical lines represent Q1 Q2 and Q3 and the wiskers on the sides extend to last values that are not outliers
				![[Pasted image 20210902132513.png|300]]
			- Outliers will represented as dots outside of the whiskers 
				![[Pasted image 20210902132542.png|300]]
	- Shape
		- Symmetric = the graph is roughly symmetrical
		- Bell-shaped (Symmetric or nearly symmetric)
		- Skewed
			- Skewed left = negatively skewed = has tail on left
			- Skewed right = positively skewed = has tail on right
		- Peak Number:
			- Unimodal: 1 peak
			- Bimodal: 2 peaks
			- Trimodal: 3 peaks
			- ...
			- Multimodal: many peaks
		- Uniform = almost flat
- Measuring center
	- [^mean]$$\text{Mean} = \frac{\sum^n_{i=1} f(x)}{n}$$
	- [^median] $$\text{Median =}\begin{cases}(\frac{n}{2}+0.5)^{th}\text{ num,} \text{ if odd}\\ \Big((\frac{n}{2})^{th}+(\frac{n}{2}+1)^{th}\Big)/2 \text{, if even}\end{cases}$$
		```py
		length = len(list)
		if length % 2 ==0:
			return (list[(length/2)-0.5] + list[(length/2)+0.5]) / 2
		else:
			return list[length/2]
		```
	- Which one to use
		- If symmetric, shouldn't be big problem which one
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
	-  $\text{Range} = \max-\min$
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
	- The formula, if not already obvious: $$z =\frac{x_i-\bar{x}}{s}$$
	- In normal distribution, the z-score, together with a z-table, can help find the percentile.
- Normal distribution
	- A kind of beautiful, perfect, symmetric, bell-shaped distribution that occur naturally
	- The distribution curve is given by this beast but never mind this isn't calculus class $$f(x)= {\frac{1}{\sigma\sqrt{2\pi}}}e^{- {\frac {1}{2}} (\frac {x-\mu}{\sigma})^2}$$
	- The **empirical rule**, a.k.a. the **68-95-99.7 rule**
		- Basically a breakdown of the distribution within whole number standard deviations away from the mean as the pic illustrates	
			![[Pasted image 20210902132551.png]]
	- Standard normal distribution
		- When dealing with theoretical distribution (viz. pure normal distribution), we use $\mu$ and $\sigma$ for mean and standard deviation to make the distinction.


[^mean]: 不会有人不知道平均数怎么求吧……
[^median]: 用了两种方法解释都没法让人看……顺带n是样本数量个数的意思，剩下的看你们理解吧，我就留在这了（不负责.jpg）