# TypeScript

TypeScript is a strongly typed programming language that is a superset of JavaScript

## Type Hinting Support

### Object Types

Object Type Declaration:
- interfaces (better for objects, they are open and can be extended)
- type declarations (better for functions)
- type alias (better for functions, they are closed and cannot be extended)

```
function greet(person: { name: string; age: number }) {
  return "Hello " + person.name;
}
```

```
interface Person {
  name: string;
  age: number;
}
 
function greet(person: Person) {
  return "Hello " + person.name;
}
```

```
type Person = {
  name: string;
  age: number;
};
 
function greet(person: Person) {
  return "Hello " + person.name;
}
```

### Property Modifiers
