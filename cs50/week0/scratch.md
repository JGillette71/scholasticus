# CS45 Week 0 - Scratch

Course is ultimately one of problem solving. Problem solving can be represented in a model of inputs and outputs.

```mermaid
flowchart LR
    node1[input]
    node2[    ]
    node3[output]

    node1 --> node2
    node2 --> node3
```

In order to problem solve and collaborate we need to be able to do so in a global or universally understood manner. For example, if we were to count we may do so by simply counting on our fingers like one, two, three, etc. This system is known as *base-1*. On a single hand, base-1 allows us to count to five. However, if we use *base-2* (binary), we can count up to 31 on each hand as each finger represents a different state.

## Representing Numbers

The concept of state in binary represents zero and one / on and off. Each representation of binary state is known as a *bit*. Compute and memory essentially consiststs of millions of transistors or switches in a state of zero or one. For example, consider we have three switches. How high can we count with a binary representation?

```plaintext
0 0 0 = 0
0 0 1 = 1
0 1 0 = 2
0 1 1 = 3
1 0 0 = 4
1 0 1 = 5
1 1 0 = 6
1 1 1 = 7
```

We have eight distinct patterns and we start count at zero, all nodes off to all nodes on, leaving us with the ability to count to seven.

Compare this to our well known decimal system (*base-10*), where each digit in a number represents a value multiplied by its placement. We see **ten** possibilities for each placeholder.

```plaintext
example: 123
(1*100) + (2*10) + (3*1)
(100) + (20) + (3) = 123
```

Translating this to binary, each placeholder is weighted by two vice ten. So we can represent digits as follows.

```plainttext
(x*4) + (x*2) + (x*1)
(x*8) + (x*4) + (x*2) + (x*1)
(x*16) + (x*8) + (x*4) + (x*2) + (x*1)
(x*32) = (x*16) + (x*8) + (x*4) + (x*2) + (x*1)
```

So we can see...

```plaintext
example: 0 1 0
(0*4) + (1*2) + (0*1) = 2
```

We can easily calculate the max value represted given the number of bits available:

```plaintext
3-bit example: 111
(1*4) + (1*2) + (1*1) = 7

8-bit example: 11111111
(1*128) + (1*64) + (1*32) + (1*16) + (1*8) + (1*4) + (1*2) + (1*1) = 255
```

There are obvious limitations to representing numbers bits alone, so we often use larger units like *Byte*. THere are **eight bits in one byte**; representing a maximum decimal value of 256 (255 + zero = 256)

## Representing Letters

It should be clear up to this point that we can represent any range of numbers using the binary system, but what about natural language, like the capital letter "A"?

There is an agreed upon standard that letters will be represented by a designated number. For example, capital "A" is represented by `01000001`, i.e., the decimal number 65. Captial "B" is represented by `01000010` or 66, and so on. Similarly, lower case "a" is `01100001`, 97, and lower case "b" is `01100010`. Bottom line is that sequences of letters are represented by designated contiguous ranges of numbers. This agreed upon standard is **ASCII**.

**ASCII** - The American Standard Code for Information Interchange

The trouble with the ASCII standard is that they only allocated 8-bits for upper case letters, lower case letters, and punctuation which limits us to 256 character representations. This is enough for english plus other latin alphabet characters but it is not enough to represent the majority of human written language.

In contrast, 32-bits would allow us to represent 4 billion different characters. This is the goal of an updated standard called **Unicode**. Unicode seeks to represent all human language past, present, and future, including pictograms like emojis. Unicode is backwards compatible with ASCII, so all english letter representations are the same.

What about **UTF-8** versus **Unicode**? Unicode Transformation Format - 8-bit (UTF-8) is a encoding standard or schema for unicode standard representations.

## Representing Color

Like letters, colors are represented by a specific system of binary values, but in this case the values are translated into a color and rendered for each pixel.Each color representation consists of three values, **RGB** or *red-green-blue*. An RGB value typically consists of three bytes (or 24 bits).

A single pixel may have a value (R:72, G:73, B:33) which renders as off-yellow. (In unicode 72, 73, 33 translates to "HI!").

When you hear of camera resolution being expressed as megabyte (MB) we know that 1 Megabyte = 1,000,000 Bytes = 8,000,000 Bits. So if each pixel has three bytes, then we know 1 Megabyte = ~333,334 pixels.

...and of course videos are just a sequence of images in terms of frames per second (FPS).

## Representing Sound

Like numbers, letters, and color, sound is represented by a standardized set of values each with a coresponding representation. An example might be a four byte set representing pitch, volume, duration, and waveform. However, we won't dive into this any more here.

## Algorithms

We now a surface level understanding of how binary represents human mediums like decimals, language, color, and sound.

```mermaid
flowchart LR
    node1[01001000,<br>01001001,<br>00100001]
    node2[program context]
    node3["HI!"]

    node1 --> node2
    node2 --> node3
```

This program context can be considered an algorithim. **An algoritim is a ***precise*** description of how to do something.** Precise step-by-step instructions to reach a desired output given an input.

Consider *divide and conquer* of phonebook versus page-by-page look-up or two-page-by-two-page lookup examples. These are precise instructions on how to solve the problem of finding the correct page in a phonebook.

```mermaid
xychart-beta
    title "CS50 Phone Book — Candidates Remaining per Step (N = 32)"
    x-axis "Step" [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16]
    y-axis "Names Remaining" 0 --> 32
    line "n (one-at-a-time)" [32,31,30,29,28,27,26,25,24,23,22,21,20,19,18,17,16]
    line "n/2 (two-at-a-time)" [32,30,28,26,24,22,20,18,16,14,12,10,8,6,4,2,0]
    line "log2(n) (binary search)" [32,16,8,4,2,1,0]
```

## Pseudocode

The act of instructing a machine with a precise set of instructions is done with **code**. When we want to translate human instructions into code, we first perform an intermediate step to help use called pseudocode.

Pseudocode allows us to write instructions that are logical, precise, and succinct yet in our own vernacular.

```plaintext
Pick up phonebook
Open to middle of book
Look for desired entry on page
If desired entry on page
    call entry
Else if entry earlier in book
    Open to middle of left half of book
    Go back to step 3
Else if desired entry in right half of the book
    Open to middle of right half of book
    Go back to step 3
Else
    quit task
```

In plain language we begin to capture key concepts like boolean expressions (yes/no), and conditional statements (if/else).

## Artificial Intelligence

Stoped at 1:03:43
