## Programming Languages: Best Practices

### PHP
- Style Guide: PSR
- Quality Control: static code analysis, profiler, unit tests, api tests
- use declare(strict_types=1) in all files to avoid type coercion in return types and arguments, without which passing a string of "1" will be accepted by this  definition "int $a" because "1" is numeric and can be coerced to an integer

### Python
- Style Guide: PEP 8
- Quality Control: static code analysis, profiler, unit tests, api tests

### JavaScript
- Use 'strict mode' directive at the top so that JavaScript doesn't allow undeclared variables (i.e. hoisting)

### TypeScript
- Style Guide: Google TypeScript
- Quality Control: static code analysis, profiler, unit tests, api tests
- use 'use strict' in all files (enables a wide range of type checking behavior that results in stronger guarantees of program correctness)
- use strictNullChecks on (when a value is null or undefined, you will need to test for those values before using methods or properties on that value)
- use compiler flag noImplicitAny so that the compiler throw an error if the type is not specified (instead of inferring any as type)
- When creating factories in TypeScript using generics, it is necessary to refer to class types by their constructor functions
- Use generics <Type> instead of type any to capture the type
- When calling a generic type, it is better to define the generic type because sometimes the compiler might not be able to use type argument inference


Generics
- generic type variables