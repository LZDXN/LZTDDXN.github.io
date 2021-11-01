# AP Computer Science Principles Quick Review

## Meta

Some concepts in the AP CSP exam are omitted in this notebook because I didn’t need them, which includes the following in case someone who is not me is looking at my notes for some reason.

1.  Data types
2.  Open source

Other things might be underexplained so be sure to investigate if anything is confusing (a simple google search usually gets you what you know). Also, do not assume everything is correct. I have probably made mistakes here and there while writing these but I will fix them as soon as I notice them.

**Table of content**

-   \[\[ #The Performance Task|The Performance Task \]\]
    -   \[\[ #Code Criteria|Code Criteria \]\]
    -   \[\[ #Video Criteria|Video Criteria \]\]
    -   \[\[ #Written Response|Written Response \]\]
    -   \[\[ #Plagiarism|Plagiarism \]\]
-   \[\[ #APCSP Contents|APCSP Contents \]\]
    -   \[\[ #Explore Curricular Requirement|Explore Curricular Requirement \]\]
    -   \[\[ #Big Idea 1: Creative Development|Big Idea 1: Creative Development \]\]
    -   \[\[ #Big Idea 2: Data|Big Idea 2: Data \]\]
    -   \[\[ #Big Idea 3: Algorithms and Programming|Big Idea 3: Algorithms and Programming \]\]
    -   \[\[ #Big Idea 4: Computing Systems and Networks|Big Idea 4: Computing Systems and Networks \]\]
    -   \[\[ #Big Idea 5: Impact of Computing|Big Idea 5: Impact of Computing \]\]
-   \[\[ #Extra|Extra \]\]

## The Performance Task

This thing accounts for 30% of the AP score

The [CB guideline](https://apcentral.collegeboard.org/pdf/ap-csp-student-task-directions.pdf) contains more detailed instructions to the performance task

The [scoring guideline](https://apcentral.collegeboard.org/pdf/ap-computer-science-principles-2021-create-performance-task-scoring-guidelines.pdf) can also be useful

An overly lengthy AP Digital Portfolio [user guide](https://apcentral.collegeboard.org/pdf/digital-portfolio-student-user-guide-ap-csp.pdf)

There’s a link somewhere on [College Board’s AP Students page](https://apstudents.collegeboard.org/) that will bring you to the digital portfolio submission page.

### Code Criteria

-   Readability
    -   Comment your code
        -   Functionality
        -   How it works
-   Must use input. The options are:
    -   Typed input
    -   Event trigger
    -   Sensor
    -   Online data stream
    -   File
-   Data storage. For example:
    -   Array
    -   Database
-   Function with
    -   At least one parameter
    -   Must call it
    -   Include these in the function
        -   Selection (if)
        -   Iteration
        -   Sequencing
-   Submit all code as `.pdf`

### Video Criteria

-   Show input being entered
-   Show functioning
-   Show output
-   Caption explaining the programming
-   No name, image, or bitmoji
-   No longer than 60 seconds
-   No larger than 30MB
-   Format can be `.mp4` `.wmv` `.avi` or `.mov`

### Written Response

College Board will provide a template for this

-   Maximum 850 words (technically 750 but there’s a 100 words buffer)
-   Label the prompts
-   Read the rubrics

### Plagiarism

According to CB

> A student who fails to acknowledge (i.e., through citation, through attribution, by reference, and/or through acknowledgment in a bibliographic entry) the source or author of any and all information or evidence taken from the work of someone else will receive a score of 0 on that particular component of the performance assessment task. 

> To the best of their ability, teachers will ensure that students understand ethical use and acknowledgment of the ideas and work of others, as well as the consequences of plagiarism. The student’s individual voice should be clearly evident, and the ideas of others must be acknowledged, attributed, and/or cited.

## APCSP Contents

### Explore Curricular Requirement

-   This is a new thing added to the course this year and there will be 5 MCQs on this topic.
-   Basically we
    -   Look at computing innovations
    -   Identify the data that they use
    -   Identify how they store data
    -   Analyse their effect
    -   Explain privacy and security concerns
-   Computing innovations can be divided into
    -   Physical innovations like GPS
    -   Non-physical software like Khan Academy
    -   Non-physical concepts like cryptocurrencies
-   Analysing data of a computing innovation, including
    -   Privacy: can someone trace to individual users using the data collected
    -   Security: who can access the data
    -   Storage: where to dump the data
    -   (Important differences: privacy is to what extent can the data be traced to individuals, whereas security is who can access the data)
-   Analysing impact of a computing innovation
    -   Effects can be positive or/and negative depending on the perspective
    -   Effects can be intended and/or unintended
-   Stimulus questions
    -   When doing these, read the question carefully and give it what it asks for
    -   Like the SAT, there must be one and only one correct answer spelt out in the question, so it would be dumb to guess
    -   Think thoroughly
    -   Bring brain to exam

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
    -   That’s why programmers seldom work alone
        -   Need example? Look how steep the learning curves of Helio Workstation, Mandelbulb 3D, and Anki are
        -   (Actually many collaborative projects are worse… never mind)
    -   Helps to spot errors
    -   Cloud technology now takes this further
        -   Look at Vivaldi and Musescore
-   Development process
    -   This is the process that brings an idea to the product
    -   The process can be flexible. It can be linear or trial and error or whatever as long as it works
    -   The development process is also often iterative, meaning that it happens a few times repeatedly
        -   This way there will be incremental improvements
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
        -   Prototyping
            -   Basically light weight simulation of how the product will work. This way testers can test the design
        -   Testing
            -   This needs to be effective and thorough
            -   Fix bugs (perhaps a way to get ten times more)
            -   Ways to reduce bug
                -   Use functions
                -   Name variables properly
                -   Draw out flow chart when confused. This is known as **Handtracing**
                -   Use IDEs (which will yell at you even when there’s no bug)
                -   Use debuggers
                -   Print everything (make sure to remove print statements by the end)
            -   Error types
                -   Syntax errors
                -   Overflow: when an integer is larger than what the programming language is happy with
                -   Runtime errors: errors that happens after being successfully compiled
                -   Logic errors: this is when you did the code wrong and it returned unexpected results.
        -   Reflection
            -   Evaluate the result to help forward the development process
-   Documentation
    -   Sometimes this is very very very helpful. When it’s not it’s better than nothing.
    -   Self documenting is when the variable names, functions, comments, and doc strings themselves explain the programme very well
    -   Comment your code
    -   Credit other people’s code
-   General
    -   An **event driven** programme is driven by user triggers
    -   The **boundary values** are the boundaries of the a programme’s accepted range. This can be tested using the boundary analysis

### Big Idea 2: Data

-   The binary system
    -   Everything is stored as binary, the combination of 0s and 1s.
    -   One zero or one is referred to as a **bit**
    -   A **byte** contains 8 bits
-   Data abstraction
    -   **Abstraction** is the process of taking complex things and generalising them
    -   We store other things that cannot be described by only two states by converting the into binary
    -   Numbers
        -   In CS, a number followed by a subscript n denotes that this number is in base n
        -   To convert number between bases, use your brain
        -   The common ones are:
            -   Base 2 or **binary**
            -   Base 8 or **octonary**
            -   Base 10 or **decimal**
            -   Base 16 or **hexadecimal**
    -   Letters
        -   People have come up with ways to encode letters into binary, store them, and decode them when needed. The mapping is more or less arbitrary so don’t worry about it.
    -   Colours
        -   RGB is probably the most common for now
        -   Modern computers commonly use 3 bytes to represent a colour, giving each channel 8 bits, so one 8-bit RGB can store 2563\=14,777,216 possible colours.
    -   Instructions
        -   Codes are converted into binary as well before the computer run them
    -   Together, there is really no way of telling what data a strong of binary digits represent because they can represent anything. Therefore, software is needed to interpret the data
-   Data errors
    -   **Overflow errors** happen when the number of bits used to represent an integer is not enough to store a number that is too big.
        -   In some programming language, the computer flips the binary digit used for storing the number’s sign after an overflow error occurs
        -   Overflow errors in some programming languages happen only when the memory limit is exceeded
    -   **Round-off errors** are when the computer cannot be precise when storing a decimal
-   Data types (analogue vs digital)
    -   **Analogue** is usually continuous, like a sound wave. It’s a continuum
    -   **Digital** data is quantised because storing continuous stuff requires infinite storage and computational power. When computers want to store analogue data, they sample the continuous thing, hoping that the later reconstructed data can approximate the original analogue data
        -   Think of Fourier transform, compressors, etc.
-   Data compression
    -   **Lossless** is when the original data can be reconstructed perfectly after compression
        -   Examples: zip, rar,
    -   **Lossy** compression is when the original data can only be approximated after compression
        -   Examples: jpeg, mp3
    -   There are trade-offs between compression techniques so use your brain
-   Dealing with data
    -   What you can do:
        -   **Cleaning**, which refers to removing or fixing broken data
        -   Filtering
        -   Classifying
        -   Find patterns, aka **data mining**
        -   Collect more to reduce **biases** present in your data
    -   Things to consider
        -   A **correlation** is when there is some relationship between data values.
            -   However, this does not imply causality
            -   Using data from multiple sources can further prove a correlation
        -   The **scalability** is how much data you can add before the programme needs to be rebuilt in another way to run properly.
            -   Cloud servers can sometimes be very scaleable
        -   **Metadata** is the extra data that is connected to the important data. This makes organising and finding data easier

### Big Idea 3: Algorithms and Programming

-   Algorithms
    -   Basically like lego pieces. Putting them together and you get your programme
    -   Ways to represent algorithm
        -   Code
        -   Natural language
        -   Flowcharts
            -   No need to draw one so no need to memorise the shapes :)
    -   Readability is important
-   Variables
    -   Variables hold data, duh
    -   They are usually stored in memory
    -   They help to “manage complexity” (An overused term by College Board)
    -   Variables can have different types
        -   Strings are strings
        -   Integers are integers
        -   Floats are floats
        -   Booleans are booleans
        -   Lists are lists
-   Logical operations
    -   AND
    -   OR
    -   NOT
    -   … (some fancier ones that are less useful)
-   Programme statements. All programmes are combinations of these statements
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
-   Analysing Algorithms
    -   In CS terms, a **problem** is a task that an algorithm cannot solve. Examples include
        -   Decision problems
        -   Optimisation problems (really?)
    -   Algorithm efficiency deals with  
        \- How long and how much memory an algorithm takes to run given datasets of different sizes
        -   Measuring efficiency
            -   Mathematically via the Big-O analysis, which won’t be on the exam
            -   Experimentally
        -   When current technology does not allow an effective solution, a **heuristic** approach is often used
            -   This is when we use more trials and errors to get close enough to get the work done

### Big Idea 4: Computing Systems and Networks

-   A **computing system** is when all sorts of computing devices work together.
    -   A **network** is created whenever two or more devices communicate with each other
        -   The connections between devices are called **paths**
            -   In small networks, the paths might just be single step like bluetooth transmission
            -   In larger networks, there are routers that send information to the next stop on the path
                -   In this case, the chosen path is usually **dynamic**, meaning that there is no fixed path, so the connection can adapt to traffic obstacles like congestion or downtime
-   The Internet
    -   It’s a network of networks connected by mostly hardware
    -   Packets and Data Streams
        -   A **data steam** is any information being transmitted using the internet
        -   When information gets send from the sending location, it’s broken down into small **packets** (of the same size (maybe except the last one)) with information about the receiving location as well as how to reconstruct the message from the packets.
        -   Then the packets get sent to the receiving location through different routes
        -   The receiving device gets all the packets and reconstruct them into the original message (même si they don’t arrive at the same time and order).
    -   Protocols
        -   Every device is known as a **node** aka **host**
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
    -   **Distributed computing systems** is what BOINC does

### Big Idea 5: Impact of Computing

-   Overview
    -   Computing innovations, like the internet, can be good and bad because fair is foul foul is fair.
        -   For example, our **Personally Identifiable Information (PII)** is becoming a problem with the development of internet
    -   The **digital divide** is the division between those who have access to internet and those who don’t as well as the results that arise therefrom
    -   Copyright is becoming a problem as copying stuff from online is easier than ever
    -   Malware is mal according to its name
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
    -   Problems
        -   Cyber bullying
        -   Misinformation
        -   Scams
        -   Crimes
        -   Discrimination
        -   etc.
-   Internet access and equality
    -   Working in the **cloud** allows people to access information and work from different places and devices
    -   The lack of internet access and/or government controlled internet access reduces the internet’s intended neutrality and inhibits some people the ability see information and speak
    -   Innovations can also be **biased**. We should try to eliminate biases that we are aware of and try to identify those that we are not aware of
    -   **Crowd-sourcing** is when individuals contribute to projects through the internet by means such as contributing computation power, data, or donation (aka **crowdfunding**)
-   Legal and Ethical Considerations
    -   Anyone that is created by a person, including their computational artifacts, is their intellectual property
    -   Using materials without citing the is a problem
    -   Making money by remixing other people’s creations is a problem
    -   Copyright types
        -   Creative Commons
            -   The creator can choose to
                1.  Freeing content globally without restrictions
                2.  Attribution alone
                3.  Attribution + ShareAlike
                4.  Attribution + Noncommercial
                5.  Attribution + Noncommercial + ShareAlike
                6.  Attribution + NoDerivatives
                7.  Attribution + Noncommercial + NoDerivatives
            -   For detail, see [Wikipedia](https://en.wikipedia.org/wiki/Creative_Commons_license)
    -   Open-source Software
        -   Omitted
    -   Open access
        -   The public sharing of data by individuals, organisations, government agencies, etc.
        -   This promotes problem solving, research, etc.
        -   However, if done wrong
            -   Peple’s PII can be leaked
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
    -   Data **security**, as previously mentioned (somewhere), deals with how well we prevent unauthorised access to data
    -   Ways to improve security
        -   Set more complicated passwords
        -   Multifactor authentication
            -   This way people need more than one layer of authentication to do things to your account or data
        -   (Store things on paper!)
-   Digital attacks, types
    -   **Phishing** attacks is when attackers create emails or websites that look legit but are not.
        -   Example: the fake Sharepoint email + the fake office login page
    -   **Viruses**
        -   Viruses infect files and transfer from computer to computer
        -   They run code on your computer and can
            -   Steal files
            -   Damage files
            -   etc.
        -   Remember, everything has a cost, including freeware
    -   **Keylogging** logs keystrokes and tries to identify passwords or other information
    -   A **rogue access point** (access point = public networks) can intercept information like password
-   Cryptography
    -   This is the study of writing secret codes and deals with
        -   Encryption
        -   Decryption
    -   **Ciphers** are coded messages and they have two parts
        -   The **key** that is used to create the secrete message
        -   The **algorithm** to that encrypts the message using a key
    -   A **symmetric cipher** is when the same key is used to encrypt and decrypt
    -   A **asymmetric cipher** uses two keys and is more common today
        -   The public key encryption uses publicly known algorithm
        -   The encrypted information is accessible to all
        -   The receiver then decrypts the message using their private key
-   Internet Security
    -   The internet uses a **trust** model, in which
        -   Digital certificates are purchased to identify trusted sites

All done :D

## Extra

-   High level programming languages have
    -   Stronger abstraction
    -   Easier to read
-   Denial-of-service attacks are when the attacker tries to deny other users’ service access by overloading the server with requests
-   Emails go through intermediate computers so they might not be very secure
-   Cookies can track and leak privacy