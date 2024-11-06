---
title: "Computer Digital Electronic"
summary: Computer Digital Electronic
date: 2023-05-05
series: ["Notes"]
weight: 1
aliases: ["/DSA"]
tags: ["Notes", "Undergraduate"]
author: ["Wahba Kamaluddin"]
---

{{< collapse summary="Chapter1:  Introductory Concepts" >}}

- 1.1 Introduction to digital 1s and 0s
  - A large part of the worldwide telecommunications system falls in the category of digital systems — used two states to represent information:
    - Telegraph system
      - short & long electric pulses
    - Morse code
      - dots & dashes
  - **Timing diagram** is used to represent the state at a given time
    ![timing diagram](https://i.stack.imgur.com/w7GYl.png)
    timing diagram
    - Voltage vs time
    - Can be produced by oscilloscope and logic analyzer
- 1.2 Digital signals
  - Transition between two states (1 → 0 or 0→1) is called edge
  - Digital circuits have input and output of 0 and 1
  - If a system operates such that the time for a complete cycle is constant, it’s called a periodic system.
- 1.3 Logic circuits and evolving technology
  - The manner which a digital circuit responds to an input is called the circuit’s logic
  - Digital circuits of today’s technology are implemented using integrated circuits (ICs) that are tailor-made for their specific function.
- 1.4 Numerical representations
  - Physical systems use quantities which must be manipulated arithmetically
  - Quantities can be represented numerically in:
    - Analog form - continuous variable
      - Sound through microphone causes voltage changes
      - speedometer changes with speed
      - mercury thermometer changes value with temperature
    - Digital form - varies in discrete steps
      - digital clock changes number for each time
      - digital thermometers show changes at least for one degree
- 1.5 Digital and analog systems
  - What is digital systems?
    - A combination of devices that manipulate logical information or physical quantities represented in digital form
    - quantities can take only discrete values
    - What are the benefits of digital systems?
      - Ease of design
      - Well suited for storing information
      - Accuracy, precision are easy to maintain
      - Programmable operation
      - Less affected by noise
      - Ease of fabrication(manufacturing) on IC chips
    - What are the limits of a digital techniques?
      - The analog nature of the world requires time-consuming conversion process
        - Convert the physical variable to an electrical signal (analog)
        - Convert the analog signal to digital form
        - Process the digital information
        - Convert the digital output back to real-world analog form
  - What is analog system?
    - A combination of devices that manipulates physical quantities represented in analog form.
    - Quantities can vary over a continuous range of values
  - Why shift to digital system?
    - Digital systems are easier to design
    - Information storage is easy
    - Accuracy, precision are easier to maintain
    - Operations can be programmed
    - Digital circuits are less affected by noise
    - More digital circuitry can be fabricated on IC chips
- 1.6 Digital number systems
  - Numbering systems:
    - Decimal - 10 symbols
    - Hexadecimal - 16 symbols
    - Octal - 8 symbols
    - Binary - 2 symbols
- 1.7 Representing binary quantities
  - How does analog signal converted into digital?
    - Taking measurements of the continuously varying signal at regular intervals
  - Examples of two state devices:
    - light bulb (off or on)
    - diode (conducting or not conducting)
    ***
    - relay (energized or not energized)
    - transistor (cutoff or saturation)
    - photocell (illuminated or dark)
    ***
- 1.8 Parallel and serial transmission
  - What is parallel transmission?
    ![Screenshot 2023-06-21 at 11.17.57 AM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_11.17.57_AM.png)
    - All bits are transmitted simultaneously
  - What is serial transmission?
    ![Screenshot 2023-06-21 at 11.18.27 AM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_11.18.27_AM.png)
    - Each bit is transmitted per some time interval
- 1.9 Memory
  - What is memory
    ![Screenshot 2023-06-21 at 11.20.21 AM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_11.20.21_AM.png)
    - A circuit that retains a response to a momentary input (if it’s 1, it’ll keep it that way until it is changed)
  - What are memory elements?
    - magnetic, optical, electronic latching circuits
- 1.10 Digital computers - What is a computer? - a system of hardware that performs arithmetic operations, manipulates data, makes decisions - it performs operations based on the instructions in teh form of a program at high speed, and a high degree of accuracy - What are the major parts in a computer?

          ![Screenshot 2023-06-21 at 11.25.36 AM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_11.25.36_AM.png)

          - Input unit - process interactions and data
          - Memory unit - stores data and instructions
          - Control unit - interprets instructions and send appropriate signals to other units as instructed
          - Arithmetic/ logic unit -  performs arithmetic calculation and logical decisions
          - Output unit - presents information form the memory to the operator or process
      - What are the types of computers?
          - Microcomputer - desktop PCs
          - Minicomputer
          - Mainframe
          - Microcontroller

  {{</ collapse >}}
  {{< collapse summary="Chapter2: Number Systems and Codes" >}}
  ![Screenshot 2023-06-21 at 12.27.04 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.27.04_PM.png)

- 2.1 Binary to decimal conversion
  - summing
    ![Screenshot 2023-05-11 at 2.14.20 PM.png](images/university-notes/CDE/Screenshot_2023-05-11_at_2.14.20_PM.png)
  - Double-dabble method
    ![Screenshot 2023-05-11 at 2.16.20 PM.png](images/university-notes/CDE/Screenshot_2023-05-11_at_2.16.20_PM.png)
- 2.2 Decimal to binary conversion
  - 1st method
    ![Screenshot 2023-05-11 at 2.18.42 PM.png](images/university-notes/CDE/Screenshot_2023-05-11_at_2.18.42_PM.png)
  - 2nd method
    ![Screenshot 2023-05-11 at 2.19.30 PM.png](images/university-notes/CDE/Screenshot_2023-05-11_at_2.19.30_PM.png)
- 2.3 Hexadecimal number system
  ![Screenshot 2023-06-21 at 12.10.13 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.10.13_PM.png)
  - Hex to decimal
    ![Screenshot 2023-06-21 at 12.11.58 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.11.58_PM.png)
  - Decimal → hex
    ![Screenshot 2023-05-11 at 2.27.02 PM.png](images/university-notes/CDE/Screenshot_2023-05-11_at_2.27.02_PM.png)
  - Hex → binary
    ![Screenshot 2023-06-21 at 12.13.40 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.13.40_PM.png)
  - Binary → hex
    ![Screenshot 2023-06-21 at 12.15.18 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.15.18_PM.png)
    - Binary is grouped to a group of 4, start converting from the LSB (most right-side)
    - Add zeros to LSB to make it 4 bits
- 2.4 What is Binary Coded Decimal (BCD)
  - A way to present decimal numbers in binary form
    ![IMG_BD5B53F66A1D-1.jpeg](images/university-notes/CDE/IMG_BD5B53F66A1D-1.jpeg)
- 2.5 What is Gray Code?
  ![binary-left, gray code-right](images/university-notes/CDE/Screenshot_2023-06-21_at_12.25.54_PM.png)
  binary-left, gray code-right
  - Used in app where numbers change rapidly
- 2.7 The byte, nibble, and word
  - 8 bits = 1 byte
  - 4 bits = 1/2 byte = nibble
  - word - a group if bits that represents a certain unit of information
    - word size - number of bits in the binary word a digital system operates on — PC = 64bits
- 2.8 Alphanumerical codes
  ![Screenshot 2023-06-21 at 12.31.00 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.31.00_PM.png)
  - represents characters and functions found on a computer keyboard:
    - 26 lowercase
    - 26 uppercase
    - 10 digits
    - 7 punctuation marks
    - others
  - consist of 7 bit, 2^7 = 128 possible codes.
- 2.9 Parity method for error detection
  ![Screenshot 2023-06-21 at 12.34.29 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_12.34.29_PM.png)
  - Binary codes are frequently moved between locations, electrical noise can cause errors during transmission
  - How to detect the error?
    - using the parity method
    - add an extra bit to a code group, called the parity bit, can be 0 or one depending on the number of 1s in the code group
    - The receiver then’ll calculate, if even/ odd, that means the code is not corrupted
    - weakness:
      - If the parity method is even (1011101), and there’s error that turns the code into even (11111111), the receiver’ll interpret it as no error, since it’s even.
    - Parity methods:
      - Even
        - The total number of bits including the parity bit must be even number
        - eg: binary group 1011 → 11011 — parity bit added to the beginning(can also be at the end) to make number of 1s even
      - Odd
        - The total number of bits including the parity bit must be odd number
        - eg: binary group 1111 → 11111 — parity bit added to the beginning(can also be at the end) to make number of 1s even
- 2.10 Applications - When ASCII character are transmitted, it must tell the receiver a new character is coming - Hence the ASCII character must be framed do that the receiver knows where the data begins and ends - the first bit, start bit must be 0 - ASCII code is sent LSB first - after MSB, a parity bit is appended to check for transmission errors - Transmission is ended by sending a stop bit (1)
  {{</ collapse >}}
  {{< collapse summary="Chapter3: Describing Logic Circuits" >}}
- What is a logical board?
  - A device that acts as a building block for digital circuits (the green boards)
- Types of logic gate:
  - AND
    ![Screenshot 2023-05-18 at 2.15.39 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.15.39_PM.png)
    ![Screenshot 2023-05-18 at 2.16.52 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.16.52_PM.png)
    - Only if both is true, the output is true
  - OR
    ![Screenshot 2023-05-18 at 2.19.07 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.19.07_PM.png)
    ![Screenshot 2023-05-18 at 2.20.15 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.20.15_PM.png)
    - One input is true, output is true
      ![Screenshot 2023-05-18 at 2.22.02 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.22.02_PM.png)
    - may be asked on exam, label the component
  - NOT
    ![Screenshot 2023-05-18 at 2.29.18 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.29.18_PM.png)
    ![Screenshot 2023-05-18 at 2.30.04 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.30.04_PM.png)
    - Also called as logical inverter (Invert the value)
  - XOR (exclusie-OR)
    ![Screenshot 2023-05-18 at 2.40.49 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.40.49_PM.png)
    ![Screenshot 2023-05-18 at 2.41.05 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.41.05_PM.png)
    - Only true if one is true, (True if input 1 and 2 is different)
  - NAND (NOT AND)
    ![Screenshot 2023-05-18 at 2.46.04 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.46.04_PM.png)
    ![Screenshot 2023-05-18 at 2.47.26 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.47.26_PM.png)
    - Invert the and logic
  - NOR (NOT OR)
    ![Screenshot 2023-05-18 at 2.48.59 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.48.59_PM.png)
    ![Screenshot 2023-05-18 at 2.49.42 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.49.42_PM.png)
  - XNOR (NOT XOR)
    ![Screenshot 2023-05-18 at 2.50.31 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.50.31_PM.png)
    ![Screenshot 2023-05-18 at 2.50.54 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.50.54_PM.png)
    - True if the input is same, false if the inputs are different
    - The most popular logic gate
- Describing Logic Circuit Algebraically
  ![Screenshot 2023-05-18 at 2.27.00 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.27.00_PM.png)
  ![Screenshot 2023-05-18 at 2.27.11 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.27.11_PM.png)
  ![Screenshot 2023-05-18 at 2.34.21 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.34.21_PM.png)
  ![Screenshot 2023-05-18 at 2.37.03 PM.png](images/university-notes/CDE/Screenshot_2023-05-18_at_2.37.03_PM.png)

{{</ collapse >}}
{{< collapse summary="Chapter4: Digital Arithmetic: Operations & Circuits" >}}

- 4.1 Binary Addition & Subtraction
  ![Screenshot 2023-06-21 at 9.03.00 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_9.03.00_PM.png)
- 4.2 Representing signed numbers
  - How to represents a negative value?
    ![Screenshot 2023-06-21 at 9.42.12 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_9.42.12_PM.png)
    - +12 is 01100
    - do 1’s complement (change 1→0 and vice-versa): 10011
    - add 1 = 10100
    - hence -12 = 10100 (since the leftmost bit is 1, means its is -16+4 =-12)
    - Why use these?
      - If there is a substraction operation, it can be represented by plus a negative number
      - eg; 12-3 = 12+(-3)
      - Hence, the complexity can be reduced
  - Slide
    - To show +ve sign, 0 is added
      ![Screenshot 2023-06-21 at 9.05.03 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_9.05.03_PM.png)
    - To show -ve sign, 1 is added
      ![Screenshot 2023-06-21 at 9.05.51 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_9.05.51_PM.png)
    - What is 2’s complement system?
      - to represent signed number
      - f number is +ve (leading 0), the 2’s complement is the same as the original number
      - steps:
        - Perform bit inversion, eg; 1101 → 0010
        - Add 1 to result, eg: 0010 + 1→ 0011
      - Why use 2’s complement?
        - (+ve bit) - (-ve bit) = (+ve )+ (negate -ve bit) — no need for a separate operation for a substraction (unified approach)
- Binary addition
  ![Screenshot 2023-06-21 at 10.06.39 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_10.06.39_PM.png)
  ![Screenshot 2023-06-21 at 10.07.38 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_10.07.38_PM.png)
- Binary subtraction
  ![Screenshot 2023-06-21 at 10.09.21 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_10.09.21_PM.png)
- 4.5 binary multiplication
  ![Screenshot 2023-06-21 at 10.15.39 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_10.15.39_PM.png)
  - when start to the next number of multiplication, move left by on(add zero to the right side)
- 4.6 Binary division
  ![Screenshot 2023-06-21 at 9.59.02 PM.png](images/university-notes/CDE/Screenshot_2023-06-21_at_9.59.02_PM.png)
- 4.7 BCD Addition
- 4.9 Arithmetic Circuits
  ![Screenshot 2023-06-01 at 2.34.40 PM.png](images/university-notes/CDE/Screenshot_2023-06-01_at_2.34.40_PM.png)

  {{</ collapse >}}
