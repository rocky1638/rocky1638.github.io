---
created_at: 2023-01-05
type: concept
aliases: []
---

# Typescript

## Basics.

- A wrapper around [[javascript]] to add typing and static analysis to JavaScript.
- We can **explicitly** type a variable like so `const a: number = 6`.
- Without a type, Typescript will implicitly assume the type of the variable.
- Common primitive types.
	- `boolean`, `number`, `string`, `any`.
	- `any` is a catch-all and shouldn’t be used typically.
- Common compound types.
	- `type[]`,
- We type a function with parameter types and a return type.
	- Common return types.
		- `void`: for when the function returns nothing.
		- `never`: for when the function will run forever/throw an error.
	- `const myFunction = (a: number, b: boolean): boolean => {}`.
- We can use generics to handle cases where we want a custom type to be a part of our type.

```javascript
interface CustomArray<T> {  
	[key: number]: T,  
	length: number,  
};

const b: CustomArray<number> = [5, 3, 246, 76];
const c: CustomArray<string> = ['allowed', 'allowed'];
```

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories::
