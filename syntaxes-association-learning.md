## Best Practices

### PHP
- use declare(strict_types=1) in all files to avoid type coercion in return types and arguments, without which passing a string of "1" will be accepted by this  definition "int $a" because "1" is numeric and can be coerced to an integer
- awareness that parent classes can access child classes by default

### Python
- awareness that parent classes cannot access child classes by default

## Interpreted vs. Compiled

### Workflow

Interpreted: 
- [1] Write code
- [2] The interpreter runs the code as is
- [3] You share your code as is (code is public) so others can run it, but they need the same interpreter

Compiled: 
- [1] Write the code
- [2] Compiler converts your code into an executable file that contains machine code (binary code)
- [3] You share the executable file (code is not public) so others can immediately run it

Compiled Steps:
- [1] Pre-processing
- [2] Compiling, 
- [3] Assembling
- [4] Linking

### Tools

Compiler Tools:
- Debugger: step through the program assembly interactively.
- Disassembler: view the program assembly in more detail.
- Decompiler, turn a program back into partial source code (assuming you know what it was written in)

### Examples
Interpreted: PHP, JavaScript \
Compiled: GoLang \
Hybrid: VisualBasic, C# (C Sharp), Java, Kotlin, Python, Swift 

### Pros
Interpreted: 
- Portable
- Easier to debug because you have access to the entire source code

Compiled:
- One executable file written in machine code
- Faster to run
- Optimized for the hardware it runs on
- Source code is private

### Cons
Interpreted: 
- Machine running code requires interpreter
- Slower
- Source code is public

Compiled: 
- Not cross-platform
- Initial compilation takes time

## Characteristics

### Python
Type: Interpreted and Compiled \
Level: High level

### JavaScript
Type: Interpreted \
Level: High level 

### PHP
Type: Interpreted \
Level: High level

### GoLang
Type: Compiled \
Level: High level (still it is considered a systems programming language) 

## Data Types (built in)

### Python (15)
String: str \
Numeric: int, float, complex \
Sequence: list, tuple, range \
Mapping: dict \
Set: set, frozen set \
Boolean: bool \
Binary: bytes, byte array, memoryview \
None: NoneType

### JavaScript (8)
String: string, \
Numeric: number, bigint \
Boolean: boolean \
None: undefined, null \
symbol \
object

### PHP (9)
String: string, \
Numeric: int, float \
Boolean: bool \
Array: arr \
Object: obj \
None: NULL, void (kind of the same but handled slightly different) \
Resource \
Callable (type signature cannot be used for this type)

### GoLang (20)
String: string \
Numeric: int8, int16, int32, int64, uint8, uint16, uint32, uint64, float32, float64, complex64, complex128 \
Boolean: bool \
Binary: byte \
Unsorted: array, slice, struct, pointer \
Unicode: rune

## Syntax Similarities and Differences

### PHP

Code Organization
- General: there is no module and package concept like in Python for code organization
- File Management: the general practice is 'one class per file' (PSR-1 standard) and namespace rules (PSR-4)
- Package Management: composer is used to install packages
- Verbosity: more verbose than Python
- Enforced Type Hinting: no (using type hinting is not mandatory)
- Operator Coercion: yes (1 + "1" will coerce "1" to 1 and no errors will be thrown; this behavior cannot be avoided)
- Type Hinting Coercion: yes (type hinting int $a will accept "1" and convert it to 1, use strict_types to avoid this behavior)

Variables
- Declaration: $variableName = 'value'
- Scoping: single scope only; 'global $variableName' makes variable globally accessible from other scopes
- Passing by reference: function foo(&$var)

Operators
- Ternary operator: $result = $condition ? 'foo' : 'bar';
- Null coalescing operator: $env = $_SERVER['APP_ENV'] ?? 'dev';
- Null safe operator (i.e. optional chaining): $array['key']?->foo

OOP
- Is Everything an Object?: no (an object is a special type that has to be explicitly defined)
- Access Modifiers: 'public' for public, 'protected' for protected, 'private' for private
- Clone objects (shallow): object = clone object
- Clone objects (deep): use special object method __clone()
- Object interface definition: interface InterfaceName()
- Object abstract definition: abstract ClassName()


### JavaScript

Code Organization
- General: there is a module concept for which there are different implementations (CommonJS, ECMAScript, TypeScript)

Variables
- Declaration: let variableName = 'value' (types of declarations: let, var, const)
- Scoping: let varName (locally/block scoped), var varName (globally scoped), const constName (locally scoped, immutable)
- Passing by reference: -

Operators
- Ternary Operator: result = isMember ? '$2.00' : '$10.00'
- Null coalescing operator: foo = null ?? 'default string';
- Optional chaining (i.e. null safe): const dogName = adventurer.dog?.name;

OOP
- Is Everything an Object?: no (everything is an object except primitives: null , undefined , strings, numbers, boolean, and symbols)
- Access Modifiers: there is no privacy
- Clone objects (shallow): const clone Food = { ...food }, const cloneFood = Object.assign({}, food)
- Clone objects (deep): JSON.parse(JSON.stringify(food)); Lodash DeepClone
- Object interface definition (TypeScript only): interface InterfaceName {} 
- Object abstract definition: -

### Python

Code Organization
- General: module and package structure (the entrypoint of a package is the \__init__.py file)
- File Management: the general practice is 'one module = one file', with one or more classes in a file
- Package Management: pip (preferred installed program) is used to install packages
- Verbosity: less verbose than PHP
- Enforced Type Hinting: no (using type hinting is not mandatory)
- Operator Coercion: no (1 + "1" will throw an exception)
- Type Hinting Coercion: no (declaration 'int varName' will raise an error if "1" is used, so it will not attempt to coerce it to 1)

Variables 
- Variable Scoping: single scope only; 'global var'  makes variable globally accessible from other scopes

OOP
- Is Everything an Object?: yes
- Access Modifiers: 'public' for public, 'protected' for protected, 'private' for private
- Object interface definition: -
- Object abstract definition (ABC package is needed): class ClassName(ABC):
