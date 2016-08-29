# Silver
Silver is general-purpose programming language, which goal is to collect many useful features from other languages, but avoid their design and working errors.

## Concepts

- Everything must be resonable
- Functional programming features: anonymous functions, first-class functions, closures
- Compound types, interfaces and extension functions will make code more familiar to OOP-users
- No automatic/implicit type conversion, static strong type system
- Statement-based language, not expression-based
- Silver compiler translates code to C language (C89 standart) for good portabilty and performance
- The core of Silver will be preserved after the full completion of its design - none of next updates will break compatibility! And compatibility won't impede the further development (as it won't affect the core)

## Features

- Literals
    - [x] Integer literals
    - [x] Floating point literals
    - [ ] List literals
    - [ ] String literals
    - [ ] Other containers literals
- Expressions
    - [x] Math expressions
    - [x] Logical expressions
    - [ ] Conditions `x in y`, `x not in y`
    - [ ] Conditional expression (`if cond: x elif cond: y else: z`)
    - [ ] Containers comprehensions (`[for x in container: expr(x)]`)
    - [ ] Lambda expressions (`lambda (x) => expr(x)`)
    - [ ] Pipe operator (`|>`)
    - [ ] Pattern matching (expr)
- Statements
    - [ ] Variables/constants definitions (**no declaration w/out definition with a value!**)
        - [ ] with type inference, if defined through value/constructor `var/let x = ...;`
        - [ ] with explicit type declaration, if defined through expression or function call `var/let x : Type = ...;`
    - [ ] Variables assignment (also augmented) `mod x = ...;`
    - [ ] Loops
        - [ ] Conditional loops: infinite, while, until, do..while, do..until
        - [ ] Container loop: `for x in container { ... }`
    - [ ] Conditional: if-elif-else
    - [ ] Procedure calling `call`
    - [ ] Pattern matching (stmnt)
- Types
    - [ ] Basic types
        - [ ] int
        - [ ] double
        - [ ] char (Unicode)
        - [ ] Сontainers with generics
            - [ ] `List<T>` (double-linked list, indexed, with all elements of type T)
            - [ ] `Set<T>` (unordered set, with all elements (no duplicates) of type T)
            - [ ] `Dict<K, T>` (associative array, with all keys (no duplicates) of type K and all elements of type T)
            - [ ] ...
        - [ ] String (based on List of Unicode characters)
        - [ ] bool (`True` and `False` -> `0` and `1` in C)
        - [ ] `None`
        - [ ] Functional type `(T): R` (in C turns to function pointer)
        - [ ] BigNum (list based, one for int and float, with ext-functions, flags NoSign, NoFloat, NoComplex and so on..)
        - [ ] ComplexNum
    - [ ] Compound types
        - [ ] Product types (namedtuple/struct) (`* x * y ...`) (made of any types)
            - [ ] With extension functions
            - [ ] With generics
        - [ ] Intersection types (`& x & y ...`) (made of product types without equal-named fields) (rename it into 'conjunction type' or smth??)
            - [ ] With extension functions
            - [ ] With generics
        - [ ] Variant types (sum/tagged union) (`| x | y ...`) (made of any types) ( http://en.wikipedia.org/wiki/Tagged_union )
            - [ ] With generics
            - [ ] `type Option<T> = | T | None;` (??)
            - [ ] Option literal `T?` -> `Option<T>`
        - [ ] Interfaces (variant types with extension functions)
            - [ ] With generics (??)
    - [ ] Type aliases (`typedef`)
        - [ ] With extension functions (??)
        - [ ] With generics (??)
- Definitions
    - [ ] Modules (to group functions and some external variables/constants for them)
    - [ ] Functions
        - [ ] `func` - for common functions
        - [ ] `proc` - for functions that don't return any value
        - [ ] `pure` - for pure functions
        - [ ] `cort` - for coroutines
    - [ ] Expression-returning functions (can be `func` and `pure`)
    - [ ] Naming function parameters in call (like in Python)
    - [ ] Multiple and keyword function parameters (like in Python)
    - [ ] Function parameters with default values (like in Python)
    - [ ] Foreign functions/types interface (at first, for C)
- Other
    - [ ] IO standart functions
    - [ ] Multiple files compilation (as a project)
    - [ ] Pure functions boost (memoization or smth)
    - [ ] Monads (?)
    - [ ] Different back-ends (?)
