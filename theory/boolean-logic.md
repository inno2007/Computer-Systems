# Boolean Logic and Expressions

This note covers Boolean algebra, logic operations, truth tables, and Boolean expressions. Boolean logic is the foundation of digital computing and binary decision-making in programming, hardware, and software systems.

---

## Boolean Algebra Basics

- **Boolean values**: Only two values — **TRUE (1)** and **FALSE (0)**
- **Operators**:
  - **AND (∙ or x)**: TRUE if all inputs are TRUE
  - **OR (+)**: TRUE if at least one input is TRUE
  - **NOT (¬ or !)**: Inverts the input

---

## Operator Behavior

### 1. AND (`A ∙ B` or `A && B`)
Returns `TRUE (1)` only if both A and B are `TRUE`.

| A | B | A ∙ B |
|---|---|--------|
| 0 | 0 |   0    |
| 0 | 1 |   0    |
| 1 | 0 |   0    |
| 1 | 1 |   1    |

---

### 2. OR (`A + B` or `A || B`)
Returns `TRUE (1)` if at least one input is `TRUE`.

| A | B | A + B |
|---|---|--------|
| 0 | 0 |   0    |
| 0 | 1 |   1    |
| 1 | 0 |   1    |
| 1 | 1 |   1    |

---

### 3. NOT (`¬A`, `A'`, or `!A`)
Returns the opposite of the input.

| A | ¬A |
|---|----|
| 0 |  1 |
| 1 |  0 |

---

## Boolean Expressions in Programming

In Java-like syntax:

- `AND`: `&&`
- `OR`: `||`
- `NOT`: `!`

Example:
```java
if (A && !B || C)
```

---

## Example Truth Table and Expression

Question: "R is TRUE when A and B are the same, and FALSE otherwise."

| A | B | R (A ≡ B) |
|---|---|-----------|
| 1 | 1 |     1     |
| 0 | 0 |     1     |
| 1 | 0 |     0     |
| 0 | 1 |     0     |

Expression:
```
R = (A ∙ B) + (¬A ∙ ¬B)
```

---

## Boolean Expression Testing Strategy

To find the correct Boolean formula:
1. Look at the output values you want (1s or 0s).
2. Try combining different conditions using AND, OR, and NOT.
3. Validate with all rows of the truth table.

---

## Advanced Boolean Example

Given:
```
A = true, B = false, C = true  
Expression: AB' + AC + BC
```

Evaluation:
```
= (1 AND NOT 0) + (1 AND 1) + (0 AND 1)  
= (1 ∙ 1) + (1 ∙ 1) + (0 ∙ 1)  
= 1 + 1 + 0 = 1 (TRUE)
```

---

## Range Testing (Boolean with Conditions)

Example:
"Write a Boolean expression to test if a number `X` is between 10 and 20 (inclusive)."

Expression:
```
(10 ≤ X) AND (X ≤ 20)
```

In Java:  
```java
if (X >= 10 && X <= 20)
```

---

This concludes the notes on Boolean logic. Up next: file systems and disk structure.
