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

Variables
- Declaration: $variableName = 'value'
- Scoping: single scope only; 'global $variableName' makes variable globally accessible from other scopes
- Passing by reference: function foo(&$var)

Operators
- Ternary operator: $result = $condition ? 'foo' : 'bar';
- Null coalescing operator: $env = $_SERVER['APP_ENV'] ?? 'dev';
- Null safe operator (i.e. optional chaining): $array['key']?->foo

OOP
- Access Modifiers: 'public' for public, 'protected' for protected, 'private' for private
- Clone objects (shallow): object = clone object
- Clone objects (deep): use special object method __clone()
- Object interface definition: interface InterfaceName()
- Object abstract definition: abstract ClassName()


### JavaScript

Variables
- Declaration: let variableName = 'value' (types of declarations: let, var, const)
- Scoping: let varName (locally/block scoped), var varName (globally scoped), const constName (locally scoped, immutable)
- Passing by reference: -

Operators
- Ternary Operator: result = isMember ? '$2.00' : '$10.00'
- Null coalescing operator: foo = null ?? 'default string';
- Optional chaining (i.e. null safe): const dogName = adventurer.dog?.name;

OOP
- Access Modifiers: there is no privacy
- Clone objects (shallow): const clone Food = { ...food }, const cloneFood = Object.assign({}, food)
- Clone objects (deep): JSON.parse(JSON.stringify(food)); Lodash DeepClone
- Object interface definition (TypeScript only): interface InterfaceName {} 
- Object abstract definition: -

### Python
- Variable Scoping: single scope only; 'global var'  makes variable globally accessible from other scopes

OOP
- Access Modifiers: 'public' for public, 'protected' for protected, 'private' for private
- Object interface definition: -
- Object abstract definition (ABC package is needed): class ClassName(ABC):
