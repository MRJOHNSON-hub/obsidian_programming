1. ###### Arithmetic 
2. ###### Assignment 


[C++ Operators](https://www.w3schools.com/cpp/cpp_operators.asp)

## 1. Arithmetic: 

* + , - ,* , / , % , increment(++) , decrement(--)
* ال modulus لا يتعامل الا مع int

> pre increment/decrement : change value first then print
> post increment/decrement : print first then change the value

---

## 2. Assignment:

= Assign --- += Addition --- -= Subtraction --- *= Multiplication --- /= Division --- %= Modulo => Remainder After division

---

## 3. comparison:

 * < , > ,<= ,>=, == , !=
* (x>y) =>true or false
>عند وضع ال comparison جوه () الاجابة بتكون true or false (1 or 0)
---

## 4. logical:

link **2 comparison operators or more**
1. && (and)  
     * `first to do`
     * the 2 must be true to get the result true
2. || (or)
    * `second to do`
    * any true to get he result true 
3. ! (not)

```c++
int x=4;
cout<<!(x < 5 && x < 10)
// not(true)= false
```

---
## 5.Bitwise:

##### 1. **AND (`&`)**

- **Operation:** Performs a bitwise AND between two operands. For each bit position, the result is 1 if both bits are 1, otherwise 0.

```c++
5 & 3    // 0101 & 0011 = 0001 (1)

```

##### 2. **OR (`|`)**

- **Operation:** Performs a bitwise OR between two operands. For each bit position, the result is 1 if at least one of the bits is 1, otherwise 0.

```c++
5 | 3    // 0101 | 0011 = 0111 (7)

```

##### 3. **XOR (`^`)**

- **Operation:** Performs a bitwise XOR (exclusive OR) between two operands. For each bit position, the result is 1 if one of the bits is 1 and the other is 0 (but not both), otherwise 0.

```c++
5 ^ 3    // 0101 ^ 0011 = 0110 (6)

```

##### 4. **NOT (`~`)**

- **Operation:** Inverts each bit of the operand. A 1 becomes 0, and a 0 becomes 1. This is a unary operator (it only takes one operand).

```c++
~5    // ~0101 = 1010 (in 4-bit, but C++ will use two's complement, so result is a negative number)

```

### 5. **Left Shift (`<<`)**

- **Operation:** Shifts the bits of the operand to the left by a specified number of positions. 

> - **Each left shift operation effectively multiplies the number by 2.

```c++
5 << 1   // 0101 << 1 = 1010 (10)

```

##### 6. **Right Shift (`>>`)**

- **Operation:** Shifts the bits of the operand to the right by a specified number of positions.

>-Each right shift operation effectively divides the number by 2, discarding the remainder. The behavior for negative numbers depends on the system and the sign extension.

```c++
5 >> 1   // 0101 >> 1 = 0010 (2)

```
---

# others:

   * unary operator (بيشتغل علي متغير واحد)
     increment / decrement  / not(~)

   * binary operators (تشتغل علي متغيرين)
      (+ -  *  /  %)

 *  ternary operator ( 3 sides : condition, true value , false value)

---
## precedence: (الاولوية)

 `1st: * , /  =then> + ,-`

>لو ليهم نفس ال precedence ابدا من الشمال لليمين
>لو في  اقواس تتفوق علي اي حاجة (parentheses=brackets)