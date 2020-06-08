# Effective Typescript Summary

My personal notes while reading "Effective TypeScript: 62 Specific Ways to Improve Your TypeScript" by [Dan Vanderkam][author]. It only contains some basic concept as my understanding. If you want to learn more, I highly recommend you should buy the book.

- [Effective Typescript website][website] - Dan posted some parts of the book as the blog post. Very interesting to read if you can't afford the full book.
- [Code Sample][github]

If you are the publisher and think this repository should not be public, please write me an email to trungk18 [at] gmail [dot] com and I will make it private.

Happy reading!

[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)][tweet]

[tweet]: https://twitter.com/intent/tweet?text=Effective%20TypeScript%20Book%20Summary&url=https://github.com/trungk18/typescript-data-structures&hashtags=typescript

## Chapter 1: Getting to Know TypeScript

### Item 1: Understand the Relationship Between TypeScript and JavaScript

- TypeScript is a superset of JavaScript. In other words, all JavaScript programs are already TypeScript programs. TypeScript has some syntax of its own, so TypeScript are not, in general, valid JavaScript programs.
  
- TypeScript adds a type system that models JavaScript's runtime behavior and tries to spot code which will throw exception at runtime. But you shouldn't it to flag every exception. It is possible for code to pass the type checker but still throw error at runtime.

```typescript
const names = ['Alice', 'Bob'];
console.log(names[2].toUpperCase());
```

- While TypeScript's type system largely models JavaScript behavior, there are some constructs that JavaScript allows but TypeScript chooses to bar, such as calling functions with wrong number of arguments. This is largely a matter of taste.

```typescript
const a = null + 7;  // Evaluates to 7 in JS
// ~~~~ Operator '+' cannot be applied to types ...

const b = [] + 12;  // Evaluates to '12' in JS
// ~~~~ Operator '+' cannot be applied to types ...

alert('Hello', 'TypeScript');  // alerts "Hello"
// ~~~~ Expected 0-1 arguments, but got 2
```

[website]: https://effectivetypescript.com/
[github]: https://github.com/danvk/effective-typescript
[author]: https://github.com/danvk