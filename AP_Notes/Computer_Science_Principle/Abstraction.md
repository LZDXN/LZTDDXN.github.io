**Abstraction**: To make complex operation easier.
Level of Abstraction:
- **High Level** examples: programming languages, they need to be compiled down to the machine code level to actually execute.
- **Low Level** examples: one step up from the machine language, which are known as "assembly" languages. They do not need to be compiled, therefore they run faster than high-level languages. 
- **Low Level Abstraction Hardware**
For example Transistor: Turn the electrical current on and off.
We do not have to know exactly how these work, just that they do work creating the basic building blocks for computers to function
- **High Level Abstraction**
For example Motherboard: controls all aspects of the computer, it is made by billions and billions of transistors

==Higher-level abstractions are combined from low-level abstractions==

### Number systems and place value
We use **decimal** system to do calculations, computer use **binary** system since they only understand on and off.

#### How Binary Numbers can be interpreted
**ACSII** stands for American Standard Code for Information Interchange. It is used to convert text to binary codes so computer can read it.
It only has 7 bits, so it can only represent 128 characters, so it is no longer in widespread use as it has been replaced by the larger Unicode table. 

![[USASCII_code_chart.png]]

**Color** (RGB)
Earlier color representations used a byte (8 bits), which can only represent 128 color. (RRRGGGBB)
We now use 256\*256\*256 possibles to represent colors -- RGB (Red Green Blue)
- Black is (0,0,0)
- White is (255,255,255)

### Logic Gates/Chips
|  A  |  B  | A AND B | A OR B | NOT A and NOT B | A XOR B |
|:---:|:---:|:-------:|:------:|:---------------:|:-------:|
|  T  |  T  |    T    |   T    |        F        |    F    |
|  T  |  F  |    F    |   T    |        F        |    T    |
|  F  |  T  |    F    |   T    |        F        |    T    |
|  F  |  F  |    F    |   F    |        T        |    F    | 


**Overflow Errors** occurs in computers when the number to be represented is larger than the computer can hold.
**Rounding or Round-off Errors** happens because the way with decimal points are stored in the computer which are imprecise and stored as a whole number + the decimal point + the fractional part of the number.

### Software: Applications and Development Environments
**Variables and Constants**: Variables, change; Constant, won't change.
**Libraries/APIs** (Application Programming Interface): A sort of programs are tested and combined in library, which are available to import into library and use in program than write long code.

**Moore's Law**: From the co-founder of Intel, Gordon Moore. He defined an observation that the number of transistors on integrated circuits doubled every two years. Though this prediction applied for many years, it does not exactly apply to the same time intervals today. (14 nm+++++++++++++++++)

**Hardware Architecture**
Computers are comprised of:
- Input
- CPU
- Control Unit
- Arithmetic/Logic Unit
- Memory
- Output

Whatever, they are not so true but right.

**Models and Simulations** are create to simplified representations of something, which save money, energy and time. They are an example of very high-level abstraction.