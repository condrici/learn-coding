# Programming Languages: Features

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
Numeric: number, bigint (numbers too large to be represented by number) \
Sequence: array \
Boolean: boolean \
Binary: not supported \
None: undefined, null \
Others: symbol, object \

### TypeScript 5 (15)
String: string, \
Numeric: number, bigint \
Sequence: array, read only array, enum, tuple, read only tuple \
Boolean: boolean \
Binary: not supported \
None: undefined, null, any, unknown, void \
Others: symbol, object \

### PHP (9)
String: string, \
Numeric: int, float \
Boolean: bool \
Sequence: array \
Binary: not supported \
None: null, void (kind of the same but handled slightly different) \
Others: Object, Resource, Callable (no type signature) \

### GoLang (20)
String: string \
Numeric: int8, int16, int32, int64, uint8, uint16, uint32, uint64, float32, float64, complex64, complex128 \
Boolean: bool \
Binary: byte \
Unsorted: array, slice, struct, pointer \
Unicode: rune

## Features Side By Side

### PHP

General Characteristics
- Objects: not everything is an object, objects are special data types
- Function types: internal, variable function, anonymous
- General: there is no module and package concept like in Python for code organization
- Variable Scoping: single scope only; 'global $variableName' makes variable globally accessible from other scopes
- File Management: the general practice is 'one class per file' (PSR-1 standard) and namespace rules (PSR-4)
- Package Management: composer is used to install packages
- Verbosity: more verbose than Python
- Operator Coercion: yes (1 + "1" will coerce "1" to 1 and no errors will be thrown; this behavior cannot be avoided)
- Type Coercion: yes (type hinting int $a will accept "1" and convert it to 1, use strict_types to avoid this behavior)
- Type Inference: yes (if the type is not defined, it will be inferred from the assigned value)

Specific Characteristics
- Parent classes can access child classes when they are extended
- Data is coerced in circumstances like calculating 1 + "1" ("1" becomes 1), no errors are thrown (cannot be disabled)
- Values passed to typed parameters are coerced, as in 'int $a' will accept "1" which is a string (can be disabled)

OOP Features
- Object Declaration: anonymous, readonly, abstract, interface
- Object constructor property promotion: yes (parameters can have their type and accessor defined)
- Method and Property Access Modifiers: public, protected, private
- Method Declaration: yes (access modifiers, return type, optional return type)
- Method Parameter Declaration: yes (type, optional type)
- Property Declaration: yes (access modifiers, type, optional type)
- Function Overloading: yes (used to dynamically create properties and methods, not the same as other languages)
- Additional features:

OOP Operations
- Clone objects (shallow): object = clone object
- Clone objects (deep): use special object method __clone()

Syntax Examples
- Ternary operator: $result = $condition ? 'foo' : 'bar';
- Null coalescing operator: $env = $_SERVER['APP_ENV'] ?? 'dev';
- Null safe operator (i.e. optional chaining): $array['key']?->foo
- Passing by reference: function foo(&$var)

### JavaScript (ECMAScript 5)

General Characteristics
- Function types: internal, variable function, anonymous, async, await
- General: there is a module concept for which there are different implementations (CommonJS, ECMAScript, TypeScript)
- Operator Coercion: yes ("" == 0 is true, 1 < x < 3 is also true for any value of x)
- Type Hinting Inference: yes (if the type is not defined, it will be inferred from the assigned value)

Specific Characteristics
- Specific features: async/await, callbacks, closures, promises
- Callbacks (functions passed to parameters are used frequently because many JavaScript actions are asynchronous)
- No concept of integer or float, everything is a number
- Types should be lower case; String, Number, BigInt and Boolean (capital letters) are legal but are special built-in objects

Variables
- Declaration: let variableName = 'value' (types of declarations: let, var, const)
- Scoping: let varName (locally/block scoped), var varName (globally scoped), const constName (locally scoped, immutable)
- Passing by reference: -

Operators
- Ternary Operator: result = isMember ? '$2.00' : '$10.00'
- Null coalescing operator: foo = null ?? 'default string';
- Optional chaining (i.e. null safe): const dogName = adventurer.dog?.name;

Built-in Functions
- Clone objects (shallow): const clone Food = { ...food }, const cloneFood = Object.assign({}, food)
- Clone objects (deep): JSON.parse(JSON.stringify(food)); Lodash DeepClone

OOP Features
- Objects: everything is an object except primitives (null , undefined , strings, numbers, boolean, and symbols)
- Access Modifiers: no
- Object interface: no
- Object abstract definition: yes
- Constructor property promotion: no

### TypeScript

Specific Characteristics
- Type Manipulation: generics, indexed access types, conditional types, mapped types, template literal types, utility types
- Settings: --strictPropertyInitialization
- No errors will be thrown if a class doesn't properly implement an interface, an abstract class will (use abstracts) 

OOP Features
- Class Access: yes (readonly)
- Class Getters and Setters: yes (syntax: get methodName(), set methodName())
- Class Signatures: yes (syntax: [s: string]: boolean | ((s: string) => boolean);)
- Class Heritage: abstract ClassName (extends AbstractClass), interface InterfaceName (implements InterfaceName)  
- Object Types: anonymous, generic (new in TypeScript)
- Access Modifiers: public, protected, private, readonly
- Method Declaration: yes (access modifiers, return type, optional return type)
- Method Parameter Declaration: yes (type, optional type)
- Property Declaration: yes (access modifiers, type, optional type, readonly type, index signature)
- Object interface: yes (defined as: interface InterfaceName(), can extend multiple interfaces)
- Object abstraction: yes (defined as: abstract ClassName())
- Constructor property promotion: yes (parameters can have their type and accessor defined)
- Function Overloading: yes (functions can have the same name but different parameters)
- Additional features: types, intersected types, generics

Variables
- Type Declarations: yes (this is usually not needed, but it is supported)

Functions
- Types: internal, anonymous, generic (new in TypeScript)
- Type annotations: parameter type, return type
- Parameters: type hint, optional parameter, optional callback parameter
- Overloading: yes
- Declare 'this' in functions: yes

Operators
- Non-null assertion operator (or null safe in PHP): x!.toFixed()
- Determine type: typeof varName (possible values: string, number, bigint, boolean, symbol, undefined, object, function) 

### Python

Characteristics
- General: module and package structure (the entrypoint of a package is the \__init__.py file)
- File Management: the general practice is 'one module = one file', with one or more classes in a file
- Package Management: pip (preferred installed program) is used to install packages
- Verbosity: less verbose than PHP
- Operator Coercion: no (1 + "1" will throw an exception)
- Type Coercion: no (declaration 'int varName' will raise an error if "1" is used, so it will not attempt to coerce it to 1)
- Type Inference: yes (if the type is not defined, it will be inferred from the assigned value)

Variables 
- Variable Scoping: single scope only; 'global var'  makes variable globally accessible from other scopes

OOP
- Is Everything an Object?: yes
- Access Modifiers: 'public' for public, 'protected' for protected, 'private' for private
- Object interface definition: -
- Object abstract definition (ABC package is needed): class ClassName(ABC):
