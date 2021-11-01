# USACO Contest Prep
```ad-todo
title: Go on the top of USACO

I am not afriad, I know what I am facing.
As long as I go on the top of the mount, that would be enough

```

I would first follow the https://usaco.guide/ which are built by previous participants, then read the book introduction of algorithm. 
# General Thing
Some information about the USACO

## Data types[^DatatypeRef]
|    Types    |           int           |          long           |          float           |          double          |     boolean      |               char               |     String     |       BigInteger       |
|:-----------:|:-----------------------:|:-----------------------:|:------------------------:|:------------------------:|:----------------:|:--------------------------------:|:--------------:|:----------------------:|
| Description |     32-big integer      |     64-bit integer      |  Single-precision float  |  Double-precision float  | True/False value |         8-bit character          |     String     | Arbitrary-size integer |
| Size (bits) |           32            |           64            |            32            |            64            | 1[^boolean_size] |                16                |    Variable    |       Unlimited        |
|    Range    | $-2^{32}$ to $2^{32}-1$ | $-2^{64}$ to $2^{64}-1$ | `-3.4E+38` to `+3.4E+38` | `-1.7E+38` to `+1.7E+38` |    true/false    | `\u0000` to `\uffff` (0 ~ 65535) | Not applicable |       Unlimited        |

[^DatatypeRef]:Referenced from https://usaco.guide/general/data-types
[^boolean_size]: Though boolean variable store only 1-bit information, in most cases data types must be aligned to bytes. 

```ad-note
title:

The large size of integers may require the use of 64-bit integer data types. 
In higher division of USACO, you need to deciside the type of the data it is going to use due to time and memory limit.
In Java, you need to cast `long	` back to `int` when accessing array indices.

```

There exist 16-bit integers `short` in both C++ and Java, however, these are generally not useful as the extra memory saved by using them. The spaces they saved is usually negligible. 

Unsigned integers (which are still whole numbers but don't have the property of `+` or `-` sign associated with them) are always non-negative (`unsigned  int`) also exist, but it is usually easier to use signed integers for most tasks. ==However, the 2-fold increase in size is sometimes the difference between overflowing and not overflowing.==

**Floating point numbers** are used to store decimal values. It is important to know that floating point numbers are not exact, since the binary architecture of computers can only store decimals to a certain precision. Hence, we should **always** expect that floating point numbers are slightly off, so it's generally a bad idea to compare two floating-point numbers for exact equality `==`.

```ad-note
title:
Contest problems will usually accommodate the inaccuracy of floating point numbers by checking if the **absolute** or **relative** diffence between your output and the answer is less than some small constant like $\epsilon = 10^{-9}$

If your output is $x$ and the answer is $y$,
- **absolute difference** is $|x-y|$
- **relative difference** is $\frac{|x-y|}{|y|}$

```
If floating point is necessary, the output format will be something along the lines of "print $10^6$" times the maximum probability of receiving exactly one accepted invitation, rounded down to the nearest integer.

**Boolean**
We'll usually use boolean to mark whether a certain process is done, and arrays of booleans to mark which components of an algorithm have finished. It require 1 byte of storage, wasting the 7 bits of storage. To use less memory, one can use bitsets (`std::bitset` in C++/`Bitset` in Java)

```ad-abstract
collapse: closed

Notes about `Java.util.BitSet`[^bitsetRef]
- **BitSet()** : A no-argument constructor to create an empty BitSet object.
- **BitSet(int no_Of_Bits)** : A one-constructor with an integer argument to create an instance of the BitSet class with an initial size of the integer argument representing the number of bits. 

Some additional notes
- *The size of the array is flexible and can grow to accommodate additional bit as needed*
- The index is *zero-based* and bit values can be accessed only by *non-negative* integers as a index.
- The default value of the BitSet is boolean false with a representation as 0 (off).
- Calling the clear method makes the bit values set to false. 
- BitSet uses about 1 bit per boolean value.
- To access a specific value in the BitSet, the get method is used with an integer argument as an index. 

[^bitsetRef]:Referenced rom https://www.geeksforgeeks.org/bitset-class-java-set-1/

```

**Character** variables represent a single character. When you access the character at a certain index within a string, the computer returns these character variable.
Character are usually represented as ACSII standard, This allows us to do arithmetic with them: Both `cout << ('f' - 'a');`(C++) and `System.out.print('f' - 'a');`(Java) will print `5`. In Java, characters are 16 bits, while in C/C++, characters are 8 bits. $\color{orange}\text{So should I learn C/C++?}$

**Strings** are stored as an array of characters. On the back end, there is an `ArrayList` updates when two strings are added. In Java, there are few methods such as `substring()` and `chatAt()` that are helpful to know. A loop can be used to access each character of an unknown string.


## Input & Output (Java) [^ioRef]

[^ioRef]: https://usaco.guide/general/input-output/#standard-io

### Standard I/O
In most websites (such as CodeForces and CSES), and in USACO problems after December 2020, input and output are **standard**.


**Method 1 -- `Scanner` and `System.out.print`**
```Java
import java.util.Scanner;

public class Main {
	static Scanner sc = new Scanner(System.in);
	public static void main(String[] args) {
		int a = sc.nextInt();
		int b = sc.nextInt();
		int c = sc.nextInt();
		System.out.print("sum is ");
		System.out.println(a + b + c);
	}
}
```
This works, but `Scanner` and `System.out.print` are slow when inputs and outputs tens of thousands of lines.

**Method 2 - `BufferedReader` and `PrintWriter`**
These are faster because they buffer the input and output and handle it all at once as opposed to parsing each line individually. However, `BufferedReader` is harder to used because it has few more methods and the `io` library must be imported for its used. A `StringTokenizer` is used to split the input line y whitespace into tokens, which are accessed individually by the `nextToken()` method.
```Java
import java.io.*;
import java.util.StringTokenizer;

public class Main {
	static BufferedReader r = new BufferedReader(new InputStreamReader(System.in));
	static PrintWriter pw = new PrintWriter(System.out);
	public static void main(String[] args) throws IOException {
		StringTokenizer st = new StringTokenizer(r.readLine());
		int a = Integer.parseInt(st.nextToken());
		int b = Integer.parseInt(st.nextToken());
		int c = Integer.parseInt(st.nextToken());
		pw.print("sum is ");
		pw.println(a + b + c);
		pw.close(); // make sure to include this line -- closes io and flushes the output
	}
}

```

**I/O Template**
The following template from Kattis's `Kattio.java`
```Java
/** Simple yet moderately fast I/O routines.
* Example usage:
* Kattio io = new Kattio(System.in, System.out);
* while (io.hasMoreTokens()) {
* int n = io.getInt();
* double d = io.getDouble();
* double ans = d*n;
* io.println("Answer: " + ans);
* *}
*io.close();
* Some notes:
* - When done, you should always do io.close() or io.flush() on the
* Kattio-instance, otherwise, you may lose output.
* - The getInt(), getDouble(), and getLong() methods will throw an
* exception if there is no more data in the input, so it is generally
* a good idea to use hasMoreTokens() to check for end-of-file.
* @author: Kattis
*/
import java.util.StringTokenizer;
import java.io.BufferedReader;
import java.io.BufferedOutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.PrintWriter;
import java.io.OutputStream;

class Kattio extends PrintWriter {
	public Kattio(InputStream i) {
		super(new BufferedOutputStream(System.out));
		r = new BufferedReader(new InputStreamReader(i));
	}
	
	public Kattio(InputStream i, OutputStream o) {
		super(new BufferedOutputStream(o));
		r = new BufferedReader(new InputStreamReader(i));
	}
	
	public boolean hasMoreTokens() {
		return peekToken() != null;
	}
	
	public int getInt() {
		return Integer.parseInt(nextToken());
	}
	
	public double getDouble() {
		return Double.parseDouble(nextToken());
	}
	
	public long getLong() {
		return Long.parseLong(nextToken());
	}
	
	public String getWord() {
		return nextToken();
	}

	private BufferedReader r;
	private String line;
	private StringTokenizer st;
	private String token;
	
	private String peekToken() {
		if (token == null)
			try {
				while (st == null || !st.hasMoreTokens()) {
					line = r.readLine();
					if (line == null)
						return null;
					st = new StringTokenizer(line);
					}
				token = st.nextToken();
				} catch (IOException e) {
				}
		return token;
	}

	private String nextToken() {
		String ans = peekToken();
		token = null;
		return ans;
		}
}
```
A shorted version modified from usaco.guide
```Java
import java.io.*;
import java.util.*;

/** Simple yet moderately fast I/O routines.
 * Some notes:
 *
 * - When done, you should always do io.close() or io.flush() on the
 *   Kattio-instance, otherwise, you may lose output.
 *
 * - The nextInt(), nextDouble(), and nextLong() methods will throw an
 *   exception if there is no more data in the input.
 *
 * @author: Kattis
 */

class Kattio extends PrintWriter {
	private BufferedReader r;
	private StringTokenizer st;
	// standard input
	public Kattio() { this(System.in,System.out); }
	public Kattio(InputStream i, OutputStream o) {
		super(o);
		r = new BufferedReader(new InputStreamReader(i));
	}
	// USACO-style file input
	public Kattio(String problemName) throws IOException {
		super(new FileWriter(problemName+".out"));
		r = new BufferedReader(new FileReader(problemName+".in"));
	}
	// returns null if no more input
	public String next() {
		try {
			while (st == null || !st.hasMoreTokens())
				st = new StringTokenizer(r.readLine());
			return st.nextToken();
		} catch (Exception e) {}
		return null;
	}
	public int nextInt() { return Integer.parseInt(next()); }
	public double nextDouble() { return Double.parseDouble(next()); }
	public long nextLong() { return Long.parseLong(next()); }
}

public class Main {
	public static void main(String[] args) {
		Kattio io = new Kattio();
		int a = io.nextInt();
		double b = io.nextDouble();
		int c = io.nextInt();
		io.print("sum is ");
		io.println(a + b + c);
		io.close(); // make sure to include this line -- closes io and flushes the output
	}
}
```

```ad-note
title: Optional: extends
`extends` is used so that `Kattio` inheris methods from `PrintWriter` (including `print()`, `println()` and `close()`). [More details](https://www.w3schools.com/java/ref_keyword_extends.asp)

```

The input methods in `Kattio` class mimic those of `Scanner`. Given an instance `io`:

|      Method       |                                                           Description                                                            |
|:-----------------:|:--------------------------------------------------------------------------------------------------------------------------------:|
|    `io.next()`    |                                 Reads the next token (up to a whitespace) and returns a `String`                                 |
|  `io.nextInt()`   |                                 Reads the next token (up to a whitespace) and returns as a `int`                                 |
|  `io.nextLong()`  |                                Reads the next token (up to a whitespace) and returns as a `long`                                 |
| `io.nextDouble()` |                               Reads the next token (up to a whitespace) and returns as a `double`                                |
|  `io.print(arg)`  |                                             Print `arg` to designated output stream                                              |
| `io.println(arg)` |                                   Prints `arg` to designated output stream and adds a newline                                    |
|   `io.close()`    | Closes the output steam and flushes the output. Make sure to call this (or `io.flush()`) at the end, or no outputs will be seen |

`````ad-seealso
title: PrintWriter Buffering

The orginal `Kattio` code had `super(new BufferedOutputStream(o));` on line 37.
But since `PrintWriter` uses buffered output, including `BufferedOutputStream` is necessary.
```Java
PrintWriter pw = new PrintWriter(new BufferedWriter(new FileWriter("problemname.out")));
```
well,
```Java
PrintWriter pw = new PrintWriter(new FileWriter("problemname.out"));
```
suffices. 

`````

```ad-seealso
title: Input speed

See [Fast I/O](https://usaco.guide/general/fast-io) for a comparison of input speeds as well as a faster method of input

```


# Bronze

## Time Complexity

### Common Complexities

|                                         Algorithms                                          |        Complexity         |
|:-------------------------------------------------------------------------------------------:|:-------------------------:|
|                                    Mathematical formulas                                    |          $O(1)$           |
|                                        Binary search                                        |        $O(\log n)$        |
|                              Ordered set/map or priority queue                              | $O(\log n)$ per operation |
| Prime factorization of an integer or checking primality/compositeness of an integer naively |       $O(\sqrt{n})$       |
|                                Reading in $n$ items of input                                |          $O(n)$           |
|                    Iterating through an array or a list of $n$ elements                     |          $O(n)$           |
|     Sorting (default sorting algorithms: mergesort, `Collections.sort`, `Arrays.sort`)      |       $O(n\log n)$        |
|    Java Quicksort `Arrays.sort` function on primitives  [^introductionToDataStructures]     |         $O(n^2)$          |
|               Iterating through all subsets of size $k$ of the input elements               |         $O(n^k)$          |
|                                Iterating through all subsets                                |         $O(2^n)$          |
|                             Iterating through all permutations                              |          $O(n!)$          |

[^introductionToDataStructures]:https://usaco.guide/bronze/intro-ds?lang=java

### Suggesting Complexities

|     |        $n$         |    Possible complexities    |     |
| --- |:------------------:|:---------------------------:| --- |
|     |     $n\le 10$      |    $O(n!),O(n^7),O(n^6)$    |     |
|     |     $n\le 20$      |   $O(2^n\cdot n),O(n^5)$    |     |
|     |     $n\le 80$      |          $O(n^4)$           |     |
|     |     $n\le 400$     |          $O(n^3)$           |     |
|     |    $n\le 7500$     |          $O(n^2)$           |     |
|     | $n\le 7\cdot 10^4$ |       $O(n\sqrt{n})$        |     |
|     | $n\le 5\cdot 10^5$ |        $O(n\log n)$         |     |
|     | $n\le 5\cdot 10^6$ |           $O(n)$            |     |
|     |   $n\le 10^{18}$   | $O(\log^2n),O(\log n),O(1)$ |     |

### Constant Factor
Constant factor refers to the idea that different operations with the same complexity take slightly different amounts of time to run. It is ignored in big-O notation.
- e.g. Three addition operations take a bit longer than a single addition operation.
- e.g.2 Although binary search on an array and insertion into an ordered set are both $O(\log n)$, binary search is noticeably faster.

If TLE (time limit exceeded) is received with the intended complexity, it is important to keep the constant factor in mind.


## Rectangle Geometry
Most problems in this category include only two or three squares or rectangles. Drawing out cases on paper should logically lead to a solution. 
https://usaco.guide/bronze/rect-geo?lang=java

## Introduction to Data Structures
A data structure determines how data is organized so that information can be used efficiently. Use the data structure wisely to solve the problem efficiently.

## Arrays
Java default `Collections` data structure are designed to store any type of object. Usually we don't want our data structures to store more type of data, so while declaring the data structure, we can put `<>` brackets:
```Java
ArrayList<String> list = new ArrayList<String>();
```
This creates an `ArrayList` structure that only stores objects of type `String`
`Collections` data types always contain an `add` method for adding an element to the collection, and a `remove` method which removes and returns a certain element from the collection. They also support `size()` method, which returns the number of elements in the data structure, and the `isEmpty()` method, which returns `true` if the data structure is empty and `false` otherwise.

## Dynamic Arrays
Dynamic arrays(`ArrayList` in Java) support all the functions that a normal array does, and can repeatedly reallocate storage to accommodate more elements as they are added. 
In a dynamic array, add and delete elements at the end in $O(1)$ time. 
```Java
// For example, here is a dynamic array and adds the numbers 1 through 10 to it
ArrayList<Integer> list = new ArrayList<Integer>();
for(int i = 1; i <= 10; i++){
	list.add(i);
}
```
In array-based contest problems, one-, two-, and three-dimensional static arrays will be used most of the time. However, we can also have static arrays of dynamic arrays, dynamic arrays of static arrays. The choice between a static array and a dynamic array is just personal preference.

## Iterating
```Java
//Two for loop: regular for loop or the for-each loop
ArrayList<Integer> list = new ArrayList<Integer>();
list.add(1); list.add(7); list.add(4); list.add(5); list.add(2);
int[] arr = {1, 7, 4, 5, 2};
for(int i = 0; i < list.size(); i++){ // regular
	System.out.println(list.get(i));
}
for(int element : arr){ // for-each
	System.out.println(element);
}
```

## Adding and Removing
Time complexity in adding and removing at any index of a dynamic array is $O(n)$ time.
```Java
ArrayList<Integer> list = new ArrayList<Integer>();
list.add(2); // [2]
list.add(3); // [2, 3]
list.add(7); // [2, 3, 7]
list.add(5); // [2, 3, 7, 5]
list.set(1, 4); // sets element at index 1 to 4 -> [2, 4, 7, 5]
list.remove(1); // removes element at index 1 -> [2, 7, 5]
// this remove method is O(n); to be avoided
list.add(8); // [2, 7, 5, 8]
list.remove(list.size()-1); // [2, 7, 5]
// here, we remove the element from the end of the list; this is O(1)
System.out.println(list.get(2)); // 5
```

## Pairs & Tuples
Used to store a collection of points on the 2D plane, <span class="red">Pairs and tuples are not available in Java's standard libraries</span>

```Java
static class Pair<K, V> {
	K first;
	V second;

	public Pair(K first_value, V second_value) {
		first = first_value;
		second = second_value;
	}
}
```
With these code written, we can use the `Pair` class:
```Java
Pair<Integer, String> p = new Pair(6, "hey");
System.out.println(p.first + " " + p.second); //6 hey
```

## Memory Allocation
Usually USACO memory limit is 256 MB.
1. Total memory size in bytes: 256MB = $256\cdot 10^6$
2. Divide by the size
	- 1 Byte:
		- `boolean`
	- 2 Bytes:
		- `char`
	- 4 Bytes:
		- `int`
		- `float`
	- 8 Bytes:
		- `long long`
		- `double`
3. Be aware that program [overhead](https://stackoverflow.com/questions/2860234/what-is-overhead) will reduce the amount of memory available.


## Sorting Methods

### Library Sorting
**Static Arrays**
Use `Arrays.sort(arr)` to sort a static array.

**Dynamic Arrays**




