# JavaScript

## Summary

Features
- Variables: var (global scope, immutable), let (block scope, mutable), const (immutable)
- Functions: statement, expression, anonymous, immediately invoked, constructor, arrow, async 
- TypeScript Compound Types: generics, indexed access types, conditional types, mapped types, template literal types, utility types
- Built-in Async Functions: setTimeout, fetch
- Specific Syntax: prototypes, async/await, promises, import/export, closures, callbacks, generators

Key Concepts
- Currying (transforms a function that receives many arguments into a sequence of functions that receive only one argument)
- Hosting (var variables only, which are immutable, can be declared after assignment without generating any errors; this can be disabled)
- Callbacks (function passed as an argument to another function; very common in JavaScript)
- Async functions ()

Key Characteristics

- It is a prototype based, object oriented language, where almost everything is an object except primitives
- TypeScript is a superset of JavaScript, think of it as a wrapper, that adds more OOP syntax support
- The prototype is an object that contains properties and methods that are inherited by objects created from a constructor
- With hoisting, you can declare variable and functions after their assignment (this happens with variables defined with 'var' only)

Best Practices
- Use 'strict mode' directive at the top so that JavaScript doesn't allow undeclared variables (i.e. hoisting)
- Put all declarations at the top of each script or function (also to avoid hosting confusion when strict mode is not used)
- In async functions is better not to use variables outside the function because that can cause unexpected behaviours

## Internals

### Workflow
1) JavaScript code is sent to the browser
2) Browser uses a "Runtime Environment" that reads the code based on a JavaScript syntax blueprint
3) For instance Google Chrome uses the "V8 Runtime Environment" (developed by The Chromium Projects at Google) that supports JavaScript version ECMAScript 6
4) The V8 Runtime Environment works fast because it compiles JavaScript into native machine code, even though JavaScript is an interpreted language

### Syntax Blueprints
- ECMAScript (blueprint for creating a scripting language that is used by JavaScript; 
the names JavaScript and ECMAScript are oftentimes used interchangeably, 
but one is the language name, the other is its blueprint)

## Module Formatting Systems

A module in JavaScript is just a file containing related code that can be accessed from other files

#### Different types of implementations
- Asynchronous Module Definition (AMD, used in browsers)
- ECMAScript Modules (the standard way, used by browsers, uses import/export statements)
- CommonJS Modules (default in NodEJS, uses require() for importing, module.exports for exporting)
- System.register format was designed to support ES6 modules within ES5
- The Universal Module Definition (UMD) can be used both in the browser and in Node.js

## JavaScript Supersets

A a superset of a programming language is an extension that introduces new features and expands the capabilities of that language

### TypeScript (most popular JavaScript superset)
- originated from the shortcomings of JavaScript
- it is not a programming language by itself, but a superset of JavaScript
- checks a program for errors before execution (i.e. "static type checking")
- never changes the runtime behavior of JavaScript code (if you move code from JavaScript to TypeScript, it is guaranteed to run the same way, even if TypeScript thinks that the code has type errors)
- adds type annotations
- adds type inference
- adds type erasure
- adds interfaces
- adds enumerated types
- adds namespaces
- adds tuples
- adds async/await
- adds Generics type hinting: type ObjectWithNameArray = Array<{ name: string }>;
- adds additional primitive types (any, unknown, never, void)
- adds composite types (type MyBool = true | false; type WindowStates = "open" | "closed" | "minimized";)
- read more: https://www.typescriptlang.org/

### TypeScript Examples
- const obj = { width: 10, height: 15 }; in JavaScript trying to access a nonexistent object property obj.heigth (has a typo) would not throw an exception, but it would rather return NaN
- console.log(4 / []); in JavaScript this would log Infinity, but TypeScript, though, considers division of number by an array to be a nonsensical operation, and will issue an error
## NodeJS

Node.js is an open-source and cross-platform runtime environment built on top of the "V8 Runtime Environment" for executing JavaScript code outside a browser, it is written in C++. Another example of a runtime environment is the Zend Engine used for PHP.

### Main Characteristics
Package Management: npm (node package manager)

## Syntax

### Function Definitions
- Statement (uses hoisting; i.e. the interpreter executes these first, when called, before running any other code)
- Expression (basic definition)
- Anonymous (used as arguments)
- Immediately Invoked (they trigger immediately, you just add () after an anonymous function)
- Constructor (function that executes in the global scope, used to create multiple objects; new Function())
- Arrow (shorthand for declaring functions)
- Async (creates a binding of a new async function to a given name)