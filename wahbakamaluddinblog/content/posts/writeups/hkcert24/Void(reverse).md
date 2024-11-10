---
title: "Void (reverse)"
summary:
date: 2024-11-10
series: ["Writeups", "Reverse", "hkcert24"]
weight: 1
aliases: ["/Void (reverse)"]
tags: ["Writeups", "Reverse", "hkcert24"]
author: ["Wahba Kamaluddin"]
---

> I made a simple webpage that checks whether the flag is correct... Wait, where are the flag-checking functions?

1. **Inspect the Page**:

   ![Screenshot 2024-11-10 at 14.49.23.png](images/writeups/hkcert24/Void(reverse)/Screenshot_2024-11-10_at_14.49.23.png)

   - Upon inspecting the webpage, there’s an empty or seemingly empty JavaScript block.
   - There’s also a link to an X post: [Link](https://x.com/aemkei/status/1843756978147078286). This post introduces the concept of hiding JavaScript code using the Hangul Filler character (`\\u3164`).

2. **Invisible Code Concept**:
   - The JavaScript code relies on the `\\u3164` character, which is an invisible Hangul Filler character, to hide the flag-checking logic.
   - The `with` block is used to access properties formed by sequences of `\\u3164`. The length of these sequences represents the binary value of the ASCII character.
3. **Proxy and Property Access**:
   - A `Proxy` object is used to intercept the property accesses within the `with` block.
   - Every time a property is accessed, the `Proxy` counts the number of `\\u3164` characters in the property name. The number of characters corresponds to an ASCII value:
     - For example, if there are 65 `\\u3164` characters in a sequence, it represents 65 (in decimal) or `01000001` in binary, which corresponds to the letter "A" in ASCII.
4. **Building JavaScript Code**:
   - The `Proxy` continues to collect these binary values with each property access. These bits are gathered until a complete JavaScript command is formed.
   - Once enough data is collected, the Proxy evaluates the constructed command using `eval()`.
5. **Decoding the Data**:

   ![Screenshot 2024-11-10 at 15.17.08.png](images/writeups/hkcert24/Void(reverse)/Screenshot_2024-11-10_at_15.17.08.png)

   - To view the constructed JavaScript code in the console, type the following:
     ```jsx
     f += String.fromCharCode((p[0] << 4) | p[1]);
     ```
