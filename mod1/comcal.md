# Combinator Calculus: A Variable-Free Programming Paradigm

---

## What is a Combinator?

- A **function without free variables**.
- A method of computation or calculation using a special notation.

---

## Overview

- A **variable-free programming language** consisting only of functions.
- A **simple, Turing-complete formalism**.
- A foundation for more advanced languages.
- A minimalist and unique computational model.

---

## SKI Calculus: Core Concepts

- Function calls are written by juxtaposing two expressions:  
  **Function** → **Argument**

### Core Combinators:
1. **Identity Combinator**:  
   $I \ x \to x$  
   *Simply returns its argument.*

2. **Constant Function**:  
   $K \ x \ y \to x$  
   *Ignores the second argument.*

3. **Generalized Application**:  
   $S \ x \ y \ z \to (x \ z) \ (y \ z)$  
   *Distributes and applies arguments.*

---

## Working with Multiple Arguments

- **Example: $K$**  
  - $K$: A well-formed program by itself; no rules apply.  
  - $K \ x$: Still no computation happens.  
  - $K \ x \ y \to x$: Executes when it has two arguments.  

- **Example: $S$**  
  - $S \ x \ y \ z \to (x \ z) \ (y \ z)$: Creates and applies function calls.

---

## Syntax and Definition

1. **Terms in SKI Calculus**:
   - $S$, $K$, and $I$ are valid terms.
   - If $x$ and $y$ are terms, then $x \ y$ is also a term.

2. **Tree Structure**:
   - Terms are represented as trees, not strings.
   - Parentheses define associations explicitly, but by default, left association applies:
     $S \ x \ y \ z = (((S \ x) \ y) \ z)$.

---

## Examples

### Simple Example:
Expression: $S \ K \ x \ y$  
- Tree Form:  
  ```
      S
     / \
    K   x
         \
          y
  ```

### Complex Example:
Expression: $(((S \ K) \ (K \ x)) \ (S \ y))$  
- Tree Form:  
  ```
            S
           / \
          K   S
         / \   \
        K   x   y
  ```

---

## Rewrite Rules

The SKI calculus operates as a **rewrite system**:  

- **Rules**:
  - $I \ x \to x$  
  - $K \ x \ y \to x$  
  - $S \ x \ y \ z \to (x \ z) \ (y \ z)$  

- **Notation**:  
  - $\to$: Single rewrite step.  
  - $\to^*$: Reflexive, transitive closure (zero or more steps).  

### Example Rewrite:
1. $S \ K \ x \ y$  
2. $\to (K \ y) \ (x \ y)$  
3. $\to y$.

---

## Conditionals in SKI Calculus

- Represent Booleans using combinators:
  - **True**: $T = K$, where $T \ x \ y \to x$.  
  - **False**: $F = S \ K$, where $F \ x \ y \to y$.  

- **Boolean Operations**:  
  - **NOT**: $\text{not } B = B \ F \ T$.  
  - **OR**: $B_1 \ \text{or } B_2 = B_1 \ T \ B_2$.  
  - **AND**: $B_1 \ \text{and } B_2 = B_1 \ B_2 \ F$.  

### Example:
$(\text{not } F) \ \text{and } T = (F \ F \ T) \ T \ F \to T$.

---

## Abstracting Functions: A Systematic Approach

1. Start with a function equation:  
   Example: $\text{swap} \ x \ y = y \ x$.

2. Eliminate variables using $S$, $K$, and $I$:
   - **Step 1**: Abstract $y$:  
     $\text{swap} \ x = S \ I \ (K \ x)$.

   - **Step 2**: Abstract $x$:  
     $\text{swap} = S (K (S \ I)) (S (K K) I)$.

---

## Recursive Functions

### Infinite Recursion:
- $(S \ I \ I) \ (S \ I \ I)$: A non-terminating expression that rewrites to itself.  
  *Example of looping behavior.*

### Factorial:
- Represent $n!$:  
  $\text{fac} \ n = (n \ \text{fac}' \ (\text{pair} \ 1 \ 1)) \ \text{first}$,  
  where:  
  - $\text{fac}' \ p = \text{pair} \ (\text{mul} \ (\text{second} \ p) \ (\text{first} \ p)) \ (\text{succ} \ (\text{second} \ p))$.

---

## Summary

- SKI calculus illustrates the power of abstraction and minimalism.
- It allows us to:
  - Define recursion, conditionals, and data structures.
  - Encode higher-order functions.
  - Explore computation from first principles.

- **Next Steps**:
  - Discuss **confluence** (guaranteeing consistent results).
  - Survey other combinator-based languages.

