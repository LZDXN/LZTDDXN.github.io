# AP Computer Science Principles Quick Review

## Meta

Some concepts in the AP CSP exam are omitted[^omi] in this notebook because I didn’t need them, which includes the following in case someone who is not me is looking at my notes for some reason.

[^omi]:Leon写omitted的地方我(或许)会补充 —— Coco

1.  Data types
2.  Open source

Other things might be underexplained so be sure to investigate if anything is confusing (a simple google search usually gets you what you know). Also, do not assume everything is correct. I have probably made mistakes here and there while writing these but I will fix them as soon as I notice them.

**Table of content**
-   AP CSP Contents
    -   Explore Curricular Requirement|Explore Curricular Requirement
    -   Big Idea 1: Creative Development|Big Idea 1: Creative Development
    -   Big Idea 2: Data|Big Idea 2: Data
    -   Big Idea 3: Algorithms and Programming|Big Idea 3: Algorithms and Programming
    -  Big Idea 4: Computing Systems and Networks|Big Idea 4: Computing Systems and Networks
    -  Big Idea 5: Impact of Computing|Big Idea 5: Impact of Computing
- Extra
## AP CSP Contents
### Explore Curricular Requirement

-   This is a new thing added to the course this year and there will be 5 MCQs on this topic.
-   Basically we
    -   Look at computing innovations
    -   Identify the data that they use
    -   Identify how they store data
    -   Analysis their effect
    -   Explain privacy and security concerns
-   Computing innovations can be divided into
    -   Physical innovations like GPS
    -   Non-physical software like Khan Academy
    -   Non-physical concepts like cryptocurrencies
-   Analyzing data of a computing innovation, including
    -   Privacy: can someone trace to individual users using the data collected
    -   Security: who can access the data
    -   Storage: where to dump the data
    -   (Important differences: privacy is to what extent can the data be traced to individuals, whereas security is who can access the data)
-   Analyzing impact of a computing innovation
    -   Effects can be positive or/and negative depending on the perspective
    -   Effects can be intended and/or unintended
-   Stimulus questions
    -   When doing these, read the question carefully and give it what it asks for
    -   Like the SAT, there must be one and only one correct answer spelt out in the question, so it would be dumb to guess
    -   Think thoroughly
    -   **Bring brain to exam** 

### Big Idea 1: Creative Development
-   Be creative with computer science and computing innovations
-   A **Computer artifact** is defined to be a thing that someone created using a computer. For example
    -   App
    -   Image
    -   3D-printed cat
    -   Useless websites
-   Purpose of collaboration
    -   Save time
    -   View issues from different perspectives
        -   Reduce bias
        -   Understand issue clearly
    -   Helps to spot errors
    -   Cloud technology now takes this further
-   Development process
    -   This is the process that brings an idea to the product
    -   The process can be flexible. It can be linear or trial and error or whatever as long as it works
    -   The development process is also often iterative, meaning that it happens a few times repeatedly
        -   This way there will be incremental[^incremental] improvements
        -   This is also how some software break down its releases to different features
    -   The steps
        -   Investigation
            -   Ask questions
            -   Understand a variety of user perspectives
            -   Define the problem
            -   Know what needs to be achieved
        -   Ideation/Design
            -   Brainstorming
            -   Storyboards
            -   Modules
                -   Basically a mind map or outline of the features needed
            -   Interface design
            -   Testing strategy
                -   Basically test user input and desired output/response
        -   Prototyping[^prototyping]
            -   Basically light weight simulation of how the product will work. This way testers can test the design
        -   Testing
            -   This needs to be effective and thorough
            -   Fix bugs (perhaps a way to get ten times more)
            -   Ways to reduce bug
                -   Use functions
                -   Name variables properly
                -   Draw out flow chart when confused. This is known as **Handtracing**[^handtracing]
                -   Use IDEs (which will yell at you even when there’s no bug)
                -   Use debuggers
                -   Print everything (make sure to remove print statements by the end)
            -   Error types
                -   **Syntax errors**: Use *help()* and check your syntax
                -   **Overflow**: when an integer is larger than what the programming language is happy with
                -   **Runtime errors**: errors that happens after being successfully compiled
                -   **Logic errors**: this is when you did the code wrong and it returned unexpected results.
        -   Reflection
            -   Evaluate the result to help forward the development process
-   Documentation
    -   Sometimes this is very very very helpful. When it’s not it’s better than nothing.
    -   Self documenting is when the variable names, functions, comments, and doc strings themselves explain the programming very well
    -   ***==Comment your code==*** (or you will regret in the future and someone will punch your face harshly)
    -   Credit other people’s code
-   General
    -   An **event driven** programming is driven by user triggers
    -   The **boundary values** are the boundaries of the a programming’s accepted range. This can be tested using the boundary analysis

[^incremental]: 增长的，逐步的
[^prototyping]: 原型
[^handtracing]: 用你的手，运行你的代码

### Big Idea 2: Data
-   The binary system
    -   Everything is stored as binary, the combination of 0s and 1s.
    -   One zero or one is referred to as a **bit**
    -   A **byte** contains 8 bits
-   Data abstraction
    -   **Abstraction** is the process of taking complex things and generalizing them[^abs]
    -   We store other things that cannot be described by only two states by converting the into binary [^highandlow]
    -   Numbers
        -   In CS, a number followed by a subscript n denotes that this number is in base n
        -   The common ones are:
            -   Base 2 or **binary**
            -   Base 8 or **octonary**
            -   Base 10 or **decimal**
            -   Base 16 or **hexadecimal**
    -   Letters
        -   People have come up with ways to encode letters into binary, store them, and decode them when needed. The mapping is more or less arbitrary so don’t worry about it.
    -   Colors
        -   RGB is probably the most common for now
        -   Modern computers commonly use 3 bytes to represent a color, giving each channel 8 bits, so one 8-bit RGB can store 256\*256\*256 =14,777,216 possible colors.
			-   Black is (0,0,0)
			- White is (255,255,255)
    -   Instructions
        -   Codes are converted into binary as well before the computer run them
    -   Together, there is really no way of telling what data a strong of binary digits represent because they can represent anything. Therefore, software is needed to interpret the data
-   Data errors
    -   **Overflow errors** happen when the number of bits used to represent an integer is not enough to store a number that is too big.
        -   In some programming language, the computer flips the binary digit used for storing the number’s sign after an overflow error occurs
        -   Overflow errors in some programming languages happen only when the memory limit is exceeded
    -   **Round-off errors** are when the computer cannot be precise when storing a decimal
-   Data types (analogue vs digital)
    -   **Analogue**[^analogue] is usually continuous, like a sound wave. It’s a continuum
    -   **Digital**[^digital] data is quantized because storing continuous stuff requires infinite storage and computational power. When computers want to store analogue data, they sample the continuous thing, hoping that the later reconstructed data can approximate the original analogue data
        -   Think of Fourier transform, compressors, etc.
-   Data compression
    -   **Lossless** is when the original data can be reconstructed perfectly after compression
        -   Examples: zip, rar
    -   **Lossy** compression is when the original data can only be approximated after compression
        -   Examples: jpeg, mp3
    -   There are ==trade-offs== between compression techniques so use your brain [^eco]
-   Dealing with data
    -   What you can do:
        -   **Cleaning**, which refers to removing or fixing broken data
        -   Filtering
        -   Classifying
        -   Find patterns, aka[^aka] **data mining**
        -   Collect more to reduce **biases** present in your data
    -   Things to consider
        -   A **correlation**[^cor] is when there is some relationship between data values.
            -   However, this does not imply causality
            -   Using data from multiple sources can further prove a correlation
        -   The **scalability**[^sca] is how much data you can add before the programming needs to be rebuilt in another way to run properly.
            -   Cloud servers can sometimes be very scaleable
        -   **Metadata** is the extra data that is connected to the important data. This makes organising and finding data easier
-   **Libraries/APIs** (Application Programming Interface) are sorts of programs are tested and combined, which are available to import into library and use in program instead of writing long code.
-   **Moore's Law**: From the co-founder of Intel, Gordon Moore. He defined an observation that the number of transistors on integrated circuits doubled every two years. 
	-   Though this prediction applied for many years, it does not exactly apply to the same time intervals today. (14 nm+++++++++++++++++)

[^abs]:High-level abstraction更容易理解和使用，比如说python等programming languages; Low-level abstraction本身非常简单（比如说0和1，开和关），但是单个动作的行为非常细微（只能是true或false），比如说直接写编译出来后的0110010110之类的，人看不懂的破东西
[^highandlow]: Higher-level abstractions are combined from low-level abstractions
[^eco]:经济学子可以出来联想了，帮助理解
[^cor]:相关性
[^sca]:可延展性
[^aka]: In case somebody doesn't know, also known as
[^analogue]: Check this [Analog and Digital](https://cdn.shopify.com/s/files/1/2476/2680/files/Picture1.png?v=1569419479)
[^digital]: 两个的区别：一个圆的(analogue)一个方的(digital)

### Big Idea 3: Algorithms and Programming
-   Algorithms
    -   Basically like lego pieces. Putting them together and you get your programming
    -   Ways to represent algorithm
        -   Code
        -   Natural language
        -   Flowcharts
            -   No need to draw one so no need to memorize the shapes :)
    -   Readability is important
-   Variables
    -   Variables hold data, duh
    -   They are usually stored in memory
    -   They help to “manage complexity” (An overused term by College Board)
    -   Variables can have different types
        -   Strings are "strings"
        -   Integers are 6666
        -   Floats are 6.0
        -   Booleans are *True*
        -   Lists are ["one stuff", "another stuff","it can also be integers"]
-   Logical operations
    -   AND
    -   OR
    -   NOT
    -   … (some fancier ones that are less useful)
    
|  A  |  B  | A AND B | A OR B | NOT A and NOT B | A XOR B (if A == B) |
|:---:|:---:|:-------:|:------:|:---------------:|:-------------------:|
|  T  |  T  |    T    |   T    |        F        |          F          |
|  T  |  F  |    F    |   T    |        F        |          T          |
|  F  |  T  |    F    |   T    |        F        |          T          |
|  F  |  F  |    F    |   F    |        T        |          F          |
-   programming statements. All programmings are combinations of these statements
    -   Sequencing
    -   Selection
    -   Iteration
-   Common algorithms
    -   Finding maximum and minimum numbers
        1.  Set min or max to first number
        2.  Compare everything else one by one to the min or max, replacing the min or max if the new number is the new min or max
    -   Finding the sum
        1.  Make an accumulator variable and set it to zero
        2.  Add the numbers one by one to the accumulator
    -   Decide if even
        1.  Return whether number mod 2 is zero
    -   Linear search aka sequential search
        -   Go for beginning to end, compare each item until found
    -   Binary search
        -   Applies only to a sorted list
        -   Start from the middle, compare if the desired value is to the left or to the right
        -   Repeat for the now narrower search range until found
-   Functions aka procedures as what College Board calls it
    -   Needs to be defined before running
    -   Needs to be called to run
    -   Can take in parameters aka arguments
    -   Can return variables
    -   There are built in functions like
        -   Print
        -   Input
    -   There are also libraries containing useful functions by other people. For example
        -   Random
-   Simulations
    -   They are just simulations
-   Analyzing Algorithms
    -   In CS terms, a **problem** is a task that an algorithm cannot solve. Examples include
        -   Decision problems
        -   Optimization problems (really?)
    -   Algorithm efficiency deals with  
        \- How long and how much memory an algorithm takes to run given datasets of different sizes
        -   Measuring efficiency
            -   Mathematically via the Big-O analysis, which won’t be on the exam
            -   Experimentally
        -   When current technology does not allow an effective solution, a **heuristic** [^heuristic] approach is often used
            -   This is when we use more trials and errors to get close enough to get the work done


[^heuristic]:启发式, enabling someone to discover or learn something for themselves

### Big Idea 4: Computing Systems and Networks
-   A **computing system** is when all sorts of computing devices work together.
    -   A **network** is created whenever two or more devices communicate with each other
        -   The connections between devices are called **paths**
            -   In small networks, the paths might just be single step like Bluetooth transmission
            -   In larger networks, there are routers that send information to the next stop on the path
                -   In this case, the chosen path is usually **dynamic**, meaning that there is no fixed path, so the connection can adapt to traffic obstacles like congestion or downtime
-   The Internet
    -   It’s a network of networks connected by mostly hardware
    -   Packets and Data Streams
        -   A **data stream** is any information being transmitted using the internet
        -   When information gets send from the sending location, it’s broken down into small **packets** (of the same size (maybe except the last one)) with information about the receiving location as well as how to reconstruct the message from the packets.
        -   Then the packets get sent to the receiving location through different routes
        -   The receiving device gets all the packets and reconstruct them into the original message (though they don’t arrive at the same time and order).
    -   Protocols
        -   Every device is known as a **node**[^node] aka **host**
        -   When devices are connected to the internet, they are given addresses
            -   The standard one is the **Internet Protocol (IP)** address
            -   Some other, perhaps older, protocols include TCP and UDP.
        -   The protocol is basically the rules that tell different devices or software how to communicate with each other in a compatible way.
    -   Fault Tolerant
        -   **Redundancy** helps to tolerate faults
            -   Sending things through multiple paths ensures that it will be received even if something is broken
    -   The **World Wide Web (WWW)**
        -   This is different from the “Internet” as WWW refers to the collection of HTML pages and documents online, not the connection between networks
    -   Hypertext Transfer Protocol (HTTP)
        -   It’s protocol used by browsers and servers to transfer web page information
        -   HTTPS is an upgraded version that is secure
-   Types of Processing
    -   **Sequential computing systems** is probably the most common because it gets most things done. Basically, one thing is done after another
    -   **Parallel computing systems** distributes code into smaller sections to be ran by different computers at the same time. This can be upscaled by adding computers to a certain point. The results from the computers in parallel are then combined. The law of diminishing return (or should it be economies of scale? whatever) applies here
    -   **Distributed computing systems** is what BOINC[^BOINC] does

[^node]:节点
[^BOINC]: https://boinc.berkeley.edu/

### Big Idea 5: Impact of Computing

-   Overview
    -   Computing innovations, like the internet, can be good and bad because fair is foul foul is fair.
        -   For example, our **Personally Identifiable Information (PII)** is becoming a problem with the development of internet
    -   The **digital divide** is the division between those who have access to internet and those who don’t as well as the results that arise therefrom
    -   Copyright is becoming a problem as copying stuff from online is easier than ever
    -   Malware is mal[^mal] according to its name
    -   Solutions to protect people’s right includes
        -   Licensing
        -   Encryption
-   Impacts of the internet
    -   Faster sharing
        -   Files
        -   Apps
        -   Information
            -   Knowledge
            -   Advertisements
            -   News
        -   etc.
    -   Easier collaboration
    -   Used in other fields, resulting in innovations in other fields.
    -   Examples of applications
        -   E-commerce
        -   Online medical stuff
        -   Navigation when lost
        -   Social medias
    -   More data
        -   Machine learning
        -   Data mining
    -   Problems[^problems]
        -   Cyber bullying (Internet troll)
        -   Misinformation
        -   Scams
        -   Crimes
        -   Discrimination
        -   etc.
-   Internet access and equality
    -   Working in the **cloud** allows people to access information and work from different places and devices
    -   The lack of internet access and/or government controlled internet access reduces the internet’s intended neutrality and inhibits some people the ability see information and speak
    -   Innovations can also be **biased**. We should try to eliminate biases that we are aware of and try to identify those that we are not aware of
    -   **Crowd-sourcing** is when individuals contribute to projects through the internet by means such as contributing computation power, data, or donation (aka **crowdfunding**)[^crowd]
-   Legal and Ethical Considerations
    -   Anyone that is created by a person, including their computational artifacts, is their intellectual property
    -   Using materials without citing the is a problem
    -   Making money by remixing other people’s creations is a problem
    -   Copyright types
        -   Creative Commons
            -   The creator can choose to [^copyrights]
                1.  Freeing content globally without restrictions
                2.  Attribution alone
                3.  Attribution + ShareAlike
                4.  Attribution + Noncommercial
                5.  Attribution + Noncommercial + ShareAlike
                6.  Attribution + NoDerivatives
                7.  Attribution + Noncommercial + NoDerivatives
    -   Open-source Software [^OpenSource]
		-   Software that is freely shared, updated, and supported by anyone who wants to do so.
    -   Open access
        -   The public sharing of data by individuals, organizations, government agencies, etc.
        -   This promotes problem solving, research, etc.
        -   However, if done wrong
            -   People’s PII can be leaked
-   Personally Identifiable Information (PII)
    -   Defined to be any data that can identify you, such as your:
        -   address
        -   age
        -   identity number
        -   birthday
        -   medical information
        -   Fingerprints
        -   etc.
    -   Pros
        -   Can help save time
    -   Cons
        -   People can track you
        -   People sell your data
    -   These information are very hard to delete once they are online, so think twice before posting. Even after we delete, they are saved by
        -   TheWaybackMachine
        -   Someone else who saw it
-   Privacy
    -   Our **digital footprints** are the small pieces of data that we leave when using digital technology that can potentially be used by others to track us. Examples include:
        -   Location
        -   Transactions
        -   Websites visited
        -   Phone pinging
        -   etc.
    -   Ways to reduce digital footprint
        -   Use a trusty browser
        -   Use proxy
        -   Block cookies
-   Data Protection
    -   Data **security**, as previously mentioned (somewhere), deals with how well we prevent unauthorized access to data
    -   Ways to improve security
        -   Set more complicated passwords
        -   Multi-factor authentication
            -   This way people need more than one layer of authentication to do things to your account or data
        -   (Store things on paper!)
-   Digital attacks, types
    -   **Phishing**[^Phishing] attacks is when attackers create emails or websites that look legit but are not.
        -   Example: the fake Sharepoint email + the fake office login page
    -   **Viruses**
        -   Viruses infect files and transfer from computer to computer
        -   They run code on your computer and can
            -   Steal files
            -   Damage files
            -   etc.
        -   Remember, everything has a cost, including freeware
    -   **Keylogging**[^keylog] logs keystrokes and tries to identify passwords or other information
    -   A **rogue access point** (access point = public networks) can intercept information like password [^rogue]
-   Cryptography
    -   This is the study of writing secret codes and deals with
        -   Encryption
        -   Decryption
    -   **Ciphers** are coded messages and they have two parts
        -   The **key** that is used to create the secrete message
        -   The **algorithm** to that encrypts the message using a key
    -   A **symmetric cipher**[^sym] is when the same key is used to encrypt and decrypt
    -   A **asymmetric cipher**[^asy] uses two keys and is more common today
        -   The public key encryption uses publicly known algorithm
        -   The encrypted information is accessible to all
        -   The receiver then decrypts the message using their private key
-   Internet Security
    -   The internet uses a **trust** model, in which
        -   Digital certificates are purchased to identify trusted sites

[^crowd]:众筹，代码和钱都行
[^mal]: ...首先Malware是恶意软件(in English), mal is bad(or wrong, in French), 所以Malware is bad hhhhhh
[^problems]:不是注解，但是the appearance of internet should not be an excuse of those 荒谬的事情发生
[^copyrights]: For detail, see [Wikipedia](https://en.wikipedia.org/wiki/Creative_Commons_license)
[^OpenSource]: 开源软件，比如说[Github](https://github.com/)是一个大型的开源代码交流平台，供大家使用以及参考学习
[^Phishing]:网络钓鱼
[^keylog]: Keylogging software does not need a physical access point, which can be downloaded onto a computer without user's knowledge.这种软件下载之后会记录用户的使用记录，通过网络发到某个节点偷取密码或权限
[^rogue]: 未授权访问点，比如说公共网络呢
[^sym]:对称加密，通过特定的算术(Reversible)达到加密的过程
[^asy]:对称加密的反义词，如果你学过化学的话，一个是one side reaction 一个是 double side.没学过的话就是不对称加密会多两个钥，一个是公钥一个是私钥. 举个例子，公钥是人人都有的锁，私钥是唯一且独特的钥匙。没有钥匙没有办法解密，只能靠猜。例子：参考比特币bit coin的原理。


All done :D[^LoL]

## Extra

-   High level programming languages have
    -   Stronger abstraction
    -   Easier to read
-   Denial-of-service attacks are when the attacker tries to deny other users’ service access by overloading the server with requests
-   Emails go through intermediate computers so they might not be very secure
-   Cookies can track and leak privacy

[^LoL]: Finally All Done...