# Number Systems and Data Representation

This note covers number systems used in computing including binary, decimal, hexadecimal, and octal. It explains how to convert between them using step-by-step methods.

---

## Types of Number Systems

| Name         | Base | Digits Used                    |
|--------------|------|--------------------------------|
| Decimal      | 10   | 0–9                            |
| Binary       | 2    | 0, 1                           |
| Octal        | 8    | 0–7                            |
| Hexadecimal  | 16   | 0–9, A(10) to F(15)            |

All number systems are **positional**, meaning the position of a digit affects its value based on the base.

---

## Decimal to Binary (Method 1 – Division by 2)

1. Divide the number by 2 repeatedly  
2. Record the remainders  
3. Read from bottom to top

Example: Convert 57 to binary  
```
57 ÷ 2 = 28 R1  
28 ÷ 2 = 14 R0  
14 ÷ 2 = 7  R0  
7 ÷ 2 = 3   R1  
3 ÷ 2 = 1   R1  
1 ÷ 2 = 0   R1  
→ Binary = 111001
```

---

## Binary to Decimal

Multiply each bit by 2^n from right to left.

Example: Convert 10110100  
```
1×2^7 + 0×2^6 + 1×2^5 + 1×2^4 + 0×2^3 + 1×2^2 + 0×2^1 + 0×2^0  
= 128 + 0 + 32 + 16 + 0 + 4 + 0 + 0 = 180
```

---

## Decimal to Hexadecimal

1. Convert decimal to binary  
2. Group binary into 4 bits (nibbles)  
3. Convert to hexadecimal using lookup

Example: 180  
Binary = 10110100  
Group: 0001 1011 0100 → Hex = 1B4

---

## Hexadecimal to Binary

Convert each hex digit to its 4-bit binary equivalent:

Example: 7A25  
```
7 = 0111  
A = 1010  
2 = 0010  
5 = 0101  
→ 0111101000100101
```

---

## Binary to Octal

Group binary digits into sets of 3 from right to left:

Example: 11101011  
```
Binary = 011101011  
Group: 011 101 011  
→ Decimal groups: 3, 5, 3  
→ Octal = 353
```

---

## Hexadecimal to Decimal

Each hex digit is multiplied by 16^position:

Example: 7A25  
```
7×16^3 + A×16^2 + 2×16^1 + 5×16^0  
= 7×4096 + 10×256 + 2×16 + 5 = 28672 + 2560 + 32 + 5 = 31269
```

---

## Octal to Decimal

Each octal digit is multiplied by 8^position:

Example: 101  
```
1×8^2 + 0×8^1 + 1×8^0 = 64 + 0 + 1 = 65
```

---

## Octal to Binary

Convert each digit into 3-bit binary:

Example: 345  
```
3 = 011  
4 = 100  
5 = 101  
→ Binary = 011100101
```

---

## Octal to Hexadecimal

1. Convert octal to binary (as above)  
2. Group into 4-bit segments from right  
3. Convert to hexadecimal

Example: 345  
Binary = 011100101  
→ Group: 0001 1100 0101  
→ Hex = 1C5

---

## Binary Addition

Like normal addition but with binary rules:

```
1 + 1 = 10 (carry 1)  
1 + 1 + carry = 11 (carry 1)  
0 + 0 = 0  
```

Example:
```
   111010  
+  101010  
= 1100100
```

---

## Binary Multiplication

Same as base-10 multiplication but uses binary addition.

---

This file helps you convert between number systems and understand how binary data is processed by computers.
