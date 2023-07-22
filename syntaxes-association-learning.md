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