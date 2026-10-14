# C Programming — Zero to Hero Notes
### Unit 1: Programming Basics + Unit 2: Decision Making & Control Flow

*(Based on your syllabus screenshot — covers Unit 1 fully and Unit 2 as shown. Send the rest of the syllabus if there are more units to add.)*

---

## PART 0: What even IS a program? (absolute zero starting point)

A **computer** only understands binary (0s and 1s). Writing directly in binary is impossible for humans, so we write instructions in a **programming language** (like C) that is easier for humans to read, and then a special program called a **compiler** translates it into binary the computer can run.

**C** is one of the oldest and most important programming languages — created by Dennis Ritchie in 1972. It's called a "middle-level language" because it's readable by humans but still lets you control hardware closely (which is why it's used in embedded systems, microcontrollers, and operating system kernels — like the note in your syllabus says).

### Key terms you must know before anything else
| Term | Meaning |
|---|---|
| Source code | The C code you write (a `.c` file) |
| Compiler | Software that converts your source code into machine code (an `.exe` or executable) |
| Compilation | The process of translating source code → machine code |
| Execution | Actually *running* the compiled program |
| Syntax | The grammar rules of the language (must be followed exactly, or you get an error) |
| Syntax error | Mistake in grammar (e.g., missing semicolon) — compiler catches this |
| Logical error | Program runs but gives wrong output (compiler can't catch this) |
| Keyword | Reserved word with special meaning (e.g., `int`, `if`, `for`) — cannot be used as a variable name |
| Identifier | Name you give to variables, functions, etc. (e.g., `age`, `total`) |

---

## TOPIC 1: Structure of a C Program

Every C program follows this fixed skeleton — **memorize this structure exactly**:

```c
#include <stdio.h>      // Preprocessor directive — includes standard input/output library

int main()              // main function — program execution ALWAYS starts here
{
    // declarations
    int a = 5;

    // statements (the actual logic)
    printf("Value is %d", a);

    return 0;            // tells the OS the program ended successfully
}
```

### Explanation of each part (this is a guaranteed 2-5 mark theory question)

1. **`#include <stdio.h>`** — This is a **preprocessor directive** (starts with `#`, processed BEFORE compilation). `stdio.h` = "standard input output header file." It gives you access to `printf()` and `scanf()` functions.

2. **`int main()`** — Every C program MUST have exactly one `main()` function. This is the **entry point** — execution always starts here, no matter where other functions are defined in the file. `int` before `main` means this function returns an integer value.

3. **Curly braces `{ }`** — Mark the beginning and end of the function's body (its "block" of code).

4. **Declaration section** — Where you declare variables and their data types before using them.

5. **Statements** — The actual instructions (calculations, printing, etc.)

6. **`return 0;`** — Ends the `main()` function and sends the value `0` back to the operating system, conventionally meaning "program finished with no errors."

7. **Semicolon `;`** — Every C **statement** must end with a semicolon. Forgetting this is the #1 beginner mistake and causes a compile error.

### Compilation and Execution Process (step-by-step — diagram-worthy answer)

```
Source Code (.c file)
        ↓
  [PREPROCESSOR]   → expands #include, #define etc. → produces expanded source code
        ↓
   [COMPILER]      → translates C code into Assembly code
        ↓
  [ASSEMBLER]      → converts assembly code into Object code (.obj file — machine code, but not linked yet)
        ↓
   [LINKER]        → links your object code with library functions (like printf's actual code) → produces Executable file (.exe)
        ↓
   [LOADER/OS]     → loads the executable into memory and CPU executes it
        ↓
      OUTPUT
```

**In one line for exam:** *Source code → Preprocessing → Compilation → Assembly → Linking → Executable → Execution → Output*

---

## TOPIC 2: Data Types, Variables, Constants

### Data Types
A **data type** tells the compiler what kind of value a variable will hold, and how much memory to reserve for it.

| Data Type | Keyword | Typical Size | Range (typical, 32-bit) | Format Specifier |
|---|---|---|---|---|
| Integer | `int` | 4 bytes | −2,147,483,648 to 2,147,483,647 | `%d` |
| Character | `char` | 1 byte | −128 to 127 | `%c` |
| Floating point | `float` | 4 bytes | ~6 decimal digits precision | `%f` |
| Double precision float | `double` | 8 bytes | ~15 decimal digits precision | `%lf` |
| Void (no value) | `void` | — | used for functions that return nothing | — |

**Modifiers** (can be added before basic types): `short`, `long`, `signed`, `unsigned`
- Example: `unsigned int` (only positive values, doubles the positive range), `long int` (bigger range)

### Variables
A **variable** is a named location in memory used to store a value that CAN change during program execution.

**Rules for naming a variable (identifier) — commonly asked:**
1. Must start with a letter or underscore `_` (NOT a digit)
2. Can contain letters, digits, underscores only (no spaces, no special characters like @, #, %)
3. Cannot be a C keyword (like `int`, `return`, `for`)
4. Case-sensitive (`Age` and `age` are different variables)

**Declaration and Initialization:**
```c
int age;            // declaration only (value is garbage/undefined until assigned)
age = 20;           // assignment
int marks = 85;     // declaration + initialization together
```

### Constants
A **constant** is a value that does NOT change during program execution.

Two ways to define constants in C:
```c
const float PI = 3.14159;      // Method 1: using 'const' keyword
#define PI 3.14159             // Method 2: using preprocessor directive (no semicolon, no data type!)
```

**Types of constants:** integer constants (`10`), floating-point constants (`10.5`), character constants (`'A'` — single quotes), string constants (`"Hello"` — double quotes).

---

## TOPIC 3: Operators (Arithmetic, Relational, Logical)

An **operator** performs an operation on one or more values (called **operands**).

### (1) Arithmetic Operators — do math

| Operator | Meaning | Example (a=10, b=3) | Result |
|---|---|---|---|
| `+` | Addition | a + b | 13 |
| `-` | Subtraction | a - b | 7 |
| `*` | Multiplication | a * b | 30 |
| `/` | Division | a / b | 3 (integer division truncates decimal!) |
| `%` | Modulus (remainder) | a % b | 1 |

**IMPORTANT trap (very commonly tested):** if BOTH operands are `int`, `/` gives only the integer part (truncates). `10/3` = `3`, NOT `3.33`. To get a decimal answer, at least one operand must be `float`/`double`: `10.0/3` = `3.33`.

Modulus `%` only works with integers, NOT floats.

### (2) Relational Operators — compare two values, result is always 1 (true) or 0 (false) in C

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `==` | equal to | 5==5 | 1 (true) |
| `!=` | not equal to | 5!=3 | 1 (true) |
| `>` | greater than | 5>3 | 1 |
| `<` | less than | 5<3 | 0 |
| `>=` | greater than or equal to | 5>=5 | 1 |
| `<=` | less than or equal to | 5<=3 | 0 |

**Common mistake:** `=` is assignment (put value INTO a variable), `==` is comparison (CHECK if two values are equal). Confusing these is a classic bug.

### (3) Logical Operators — combine multiple conditions

| Operator | Meaning | Example | Explanation |
|---|---|---|---|
| `&&` | Logical AND | (a>5 && b<10) | TRUE only if BOTH conditions are true |
| `\|\|` | Logical OR | (a>5 \|\| b<10) | TRUE if AT LEAST ONE condition is true |
| `!` | Logical NOT | !(a>5) | Reverses the result (true→false, false→true) |

**In C, `0` means false, and any non-zero value means true.**

### Other operators you should know
- **Assignment:** `=`, and compound: `+=`, `-=`, `*=`, `/=`, `%=` (e.g., `a += 5` means `a = a + 5`)
- **Increment/Decrement:** `++` (increases by 1), `--` (decreases by 1)
  - **Pre-increment** `++a`: increases value FIRST, then uses it
  - **Post-increment** `a++`: uses the current value FIRST, then increases it
  - Example: if a=5, `printf("%d", a++)` prints `5` (then a becomes 6). `printf("%d", ++a)` prints `6` immediately.

### Operator Precedence (which runs first) — simplified order (high to low)
1. `()` parentheses
2. `++` `--` (unary)
3. `*` `/` `%`
4. `+` `-`
5. `<` `<=` `>` `>=`
6. `==` `!=`
7. `&&`
8. `||`
9. `=` (assignment)

**Tip:** When in doubt, use parentheses `()` to force the order you want — it's always safe and often expected in exams.

---

## TOPIC 4: Input/Output — `scanf` and `printf`

### `printf()` — used to DISPLAY output on screen
```c
printf("format string", variable1, variable2, ...);
```
Example:
```c
int age = 20;
printf("My age is %d years", age);   // Output: My age is 20 years
```

### `scanf()` — used to TAKE INPUT from the user
```c
scanf("format specifier", &variable);
```
Example:
```c
int age;
scanf("%d", &age);     // NOTE the & (address-of operator) — very commonly forgotten/tested!
```

**Why the `&` in scanf?** `scanf` needs to know the **memory address** of the variable to store the input value directly into it. `&variable` means "address of variable." (printf does NOT need `&` because it only reads the value, doesn't need to write into it.)

### Common Format Specifiers
| Specifier | Used for |
|---|---|
| `%d` | int |
| `%f` | float |
| `%lf` | double (in scanf; printf accepts %f for double too) |
| `%c` | char |
| `%s` | string |
| `%x` | hexadecimal |
| `%o` | octal |

### Full example program (classic exam-style)
```c
#include <stdio.h>
int main()
{
    int a, b, sum;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    sum = a + b;
    printf("Sum = %d", sum);
    return 0;
}
```

---

## TOPIC 5: Type Conversion

**Type conversion** means converting one data type into another.

### (1) Implicit Type Conversion (Automatic — done by compiler)
The compiler automatically converts a smaller data type to a larger one when needed (this is called "type promotion") to avoid data loss.
```c
int a = 5;
float b = a;    // int automatically converted to float → b = 5.000000
```
Order (smaller → larger): `char → int → float → double`

### (2) Explicit Type Conversion (Type Casting — done manually by programmer)
You force a conversion using `(datatype)` before the value.
```c
int a = 5, b = 2;
float result = (float)a / b;   // forces a to become float BEFORE division → result = 2.5
```
Without the cast: `float result = a/b;` would compute `5/2` as integer division first (=2), THEN convert to float (=2.000000) — **wrong answer!** This exact trap is a favorite numerical/output-prediction question.

### Simple Expressions
An **expression** is any valid combination of variables, constants, and operators that evaluates to a value.
```c
int result = (a + b) * c - d / 2;
```
Follow operator precedence rules above to solve step by step.

---

## TOPIC 6: Control Statements (Decision Making)

Normally, a C program executes statements **top to bottom, one after another** (sequential execution). **Control statements** let you change this flow — either by making decisions (if the program should do A or B) or by repeating a block (loops).

### (1) `if` statement — do something ONLY IF a condition is true
```c
if (condition)
{
    // executes only if condition is true (non-zero)
}
```
Example:
```c
if (age >= 18)
{
    printf("Eligible to vote");
}
```

### (2) `if-else` statement — do A if true, otherwise do B
```c
if (condition)
{
    // block A
}
else
{
    // block B
}
```
Example:
```c
if (num % 2 == 0)
    printf("Even");
else
    printf("Odd");
```

### (3) Nested `if` — an if statement inside another if statement
```c
if (a > b)
{
    if (a > c)
        printf("a is largest");
}
```

### (4) `if-else-if` ladder — check multiple conditions in sequence
```c
if (marks >= 90)
    printf("Grade A");
else if (marks >= 75)
    printf("Grade B");
else if (marks >= 50)
    printf("Grade C");
else
    printf("Fail");
```
**How it works:** conditions are checked top to bottom; as soon as ONE is true, that block runs and the rest are skipped.

### (5) `switch` statement — cleaner alternative to a long if-else-if ladder when comparing ONE variable against multiple fixed values
```c
switch(expression)
{
    case value1:
        // code
        break;
    case value2:
        // code
        break;
    default:
        // code if no case matches
}
```
Example:
```c
switch(day)
{
    case 1: printf("Monday"); break;
    case 2: printf("Tuesday"); break;
    default: printf("Invalid day");
}
```
**Important:** `break` is needed after each case, otherwise execution "falls through" into the next case automatically (this fall-through behavior is a classic trick question — always mention it).

---

## TOPIC 7: Loops — for, while, do-while

Loops let you **repeat a block of code multiple times** without writing it again and again.

### (1) `for` loop — used when you know how many times to repeat in advance

```c
for(initialization; condition; update)
{
    // code to repeat
}
```
Example — print 1 to 5:
```c
for(int i = 1; i <= 5; i++)
{
    printf("%d ", i);
}
// Output: 1 2 3 4 5
```
**How it works (memorize this exact order — very commonly asked):**
1. `initialization` runs ONCE at the start (`i = 1`)
2. `condition` is checked (`i <= 5`) — if true, go to step 3; if false, loop ends
3. Loop body executes
4. `update` runs (`i++`)
5. Go back to step 2, repeat

### (2) `while` loop — used when you DON'T know exact number of repetitions in advance (condition-controlled), condition checked BEFORE each iteration

```c
while(condition)
{
    // code to repeat
    // update statement (must be inside, or infinite loop!)
}
```
Example:
```c
int i = 1;
while(i <= 5)
{
    printf("%d ", i);
    i++;
}
```

### (3) `do-while` loop — same as while, BUT condition is checked AFTER the loop body runs

```c
do
{
    // code
} while(condition);      // note the semicolon here!
```
Example:
```c
int i = 1;
do
{
    printf("%d ", i);
    i++;
} while(i <= 5);
```

**KEY DIFFERENCE (guaranteed theory question):** In `while`, condition is checked FIRST — if false initially, the loop body never runs even once. In `do-while`, the body runs AT LEAST ONCE, no matter what, because the condition is checked only AFTER the first execution.

### Comparison Table (for/while/do-while)
| Loop | Condition checked | Minimum executions | Best used when |
|---|---|---|---|
| `for` | Before each iteration | 0 (if condition false initially) | Number of iterations is known |
| `while` | Before each iteration | 0 | Number of iterations unknown, condition-based |
| `do-while` | After each iteration | 1 (always runs at least once) | Need guaranteed at least one execution (e.g., menu-driven programs) |

### `break` and `continue`

**`break`** — immediately EXITS the loop entirely (skips all remaining iterations).
```c
for(int i = 1; i <= 10; i++)
{
    if(i == 5)
        break;          // loop stops completely when i becomes 5
    printf("%d ", i);
}
// Output: 1 2 3 4
```

**`continue`** — skips the REST of the current iteration only, and jumps to the next iteration (loop keeps running).
```c
for(int i = 1; i <= 5; i++)
{
    if(i == 3)
        continue;       // skips printing 3, but loop continues
    printf("%d ", i);
}
// Output: 1 2 4 5
```

**One-line difference to write in exam:** *`break` terminates the loop completely; `continue` skips only the current iteration and moves to the next one.*

---

## QUICK PRACTICE — Predict the Output (classic exam question type)

```c
int a = 5, b = 2;
printf("%d", a/b);        // Answer: 2 (integer division)
printf("%f", (float)a/b); // Answer: 2.500000
printf("%d", a%b);        // Answer: 1
```

```c
int i;
for(i=1; i<=3; i++)
{
    printf("%d ", i);
}
// Answer: 1 2 3
```

```c
int x = 10;
if(x > 5)
    printf("A");
else if(x > 8)
    printf("B");
else
    printf("C");
// Answer: A  (once a true condition is found, rest are SKIPPED — even if also true)
```

---

## MASTER QUICK-REFERENCE (revise this right before exam)

| Concept | Key Syntax |
|---|---|
| Basic structure | `#include`, `int main(){ }`, `return 0;` |
| Compilation flow | Source → Preprocess → Compile → Assemble → Link → Execute |
| Print output | `printf("%d", var);` |
| Take input | `scanf("%d", &var);` (don't forget `&`) |
| Type cast | `(float)a / b` |
| if-else | `if(cond){}else{}` |
| switch | `switch(x){case 1: ...; break; default: ...;}` |
| for loop | `for(init; cond; update){}` |
| while loop | checks condition BEFORE running |
| do-while loop | checks condition AFTER running (runs ≥1 time) |
| break | exits loop completely |
| continue | skips current iteration only |

## LIKELY EXAM QUESTIONS
1. Explain the structure of a C program with a diagram.
2. Explain the compilation and execution process of a C program.
3. Differentiate between `while` and `do-while` loop.
4. Differentiate between `break` and `continue`.
5. What is the difference between implicit and explicit type conversion? Give an example.
6. Write a program using switch-case (e.g., simple calculator).
7. Write a program to check if a number is prime/even-odd/leap year using if-else and loops.
8. Predict-the-output questions on operator precedence, pre/post increment, and integer division.
9. Explain operator precedence with example.
10. What is the difference between `=` and `==`?

---

**Note:** This covers Unit 1 fully and Unit 2 as visible in your screenshot (Control Statements + Loops + break/continue). If your paper also covers **Arrays, Strings, Functions, Pointers, or Structures**, send that part of the syllabus and I'll add those units in the same format right away.
