#csa
- [[#Unit 1 - Primitive Types]]
[[Transfer from Python to Java]]


# Unit 1 - Primitive Types
- **syntax** :: The correct way to type the code sot he program will run
- **compiler** :: In computing, a compiler is a computer program that translates computer code written in one programming language (the source language) into another language (the target language).

## Different Data Types in Java

![[Pasted image 20210906102958.png|500]]

| Data Type | Default Value | Default Size |                                                          |
|:---------:|:-------------:|:------------:|:--------------------------------------------------------:|
|  boolean  |     false     |    1 bit     |                  only two possible way                   |
|   char    |   '\u0000'    |    2 byte    |                      16-bit Unicode                      | 
|   byte    |       0       |    1 byte    |                       8-bit signed                       |
|   short   |       0       |    2 byte    |                      16-bit signed                       |
|    int    |       0       |    4 byte    |                      32-bit signed                       |
|   long    |      0L       |    8 byte    |                      64-bit signed                       |
|   float   |     0.0f      |    4 byte    | 32-bit IEEE 754 floating point, value range is unlimited |
|  double   |     0.0d      |    8 byte    | 64-bit IEEE 754 floating point, value range is unlimited |

\*Java uses Unicode system not ASCII code system


# Unit 2 - Using Objects

# Unit 3 - Boolean Expressions and if Statements
## Relational Operators
- **condition** ::: A comparison of two values using a relational operator.
- **assignment operator** ::: Single equals **=**, is used for assigning values to a variable.
- **not operator** ::: Exclamation point **!**, is referred to as a **negation** operator

Difference between \== and .equals()[^difference-equals-method-java]
- **address comparison** ::: Double equals **\==**
-  **content comparison** ::: .equals()

[^difference-equals-method-java]: From https://www.geeksforgeeks.org/difference-equals-method-java/

|        Comparison        | Java Symbol |
|:------------------------:|:-----------:|
|       Greater than       |     $>$     |
|        Less than         |     $<$     |
| Greater than or equal to |    $>=$     |
|  Less than or equal to   |    $<=$     |
|         Euqal to         |    $==$     |
|       Not equal to       |    $!=$     |

## Logical Operators
| Logical Operator | Java Symbol | Compound Conditional |     Result with Explanation      |
|:----------------:|:-----------:|:--------------------:|:--------------------------------:|
|       AND        |     &&      |        A && B        | True if all true, else is False  |
|        OR        |    \|\|     |       A \|\| B       | False if all false, else is True |

### The Truth Table
| First Operand(A) | Second Operand(B) | A && B | A \|\| B |
|:----------------:|:-----------------:|:------:|:--------:|
|        T         |         T         |   T    |    T     |
|        T         |         F         |   F    |    T     |
|        F         |         T         |   F    |    T     |
|        F         |         F         |   F    |    F     |



# Unit 4 - Iteration

# Unit 5 - Writing Classes
- method ::: The formal names given to the data that gets passed into a method.

# Unit 6 - Array

# Unit 7 - Array List

# Unit 8 - 2D Array

# Unit 9 - Inheritance

# Unit 10 - Recursion