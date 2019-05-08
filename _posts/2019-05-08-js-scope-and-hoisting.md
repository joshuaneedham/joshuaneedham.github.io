---
published: true
---
## Scope

> Scope - From MDN Reference
>
> > The current context of execution. The context in which values and **expressions** are "visible," or can be referenced. If a **variable** or other expression is not "in the current scope," then it is unavailable for use. Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.

### What is "Scope"?

_**Scope**_ as it pertains to Javascript is the region in a program where a variable can be accessed.

#### Global Scope - Variables defined outside of a function are "Global"

```js
//Global 'let' Scope Example
let globalLetVariable = "Global 'let' Variable";
function globalScopeVariable() {
	if (true) {
		console.log(globalLetVariable);
	}
}
```

If we run `globalScopeVariable();` we get the following output:

```console
globalScopeVariable();
Global 'let' Variable
=> undefined
```

#### Local Scope - Variables defined inside of a function are "Local"

```js
//Local 'let' Scope Example
function es6LetScopedVariable() {
	if (true) {
		let localLetVariable = "Local 'let' Variable";
	}
	console.log(localLetVariable);
}
```

Running `es6LetScopedVariable();` results in the following output due to `let` declared variables not being available outside of block in which is it defined(between the `{}` curly brackets):

```console
ReferenceError: localVariable is not defined
    at localScopeVariable (evalmachine.<anonymous>:5:14)
    at evalmachine.<anonymous>:1:1
    at Script.runInContext (vm.js:107:20)
    at Object.runInContext (vm.js:285:6)
    at evaluate (/run_dir/repl.js:133:14)
    at ReadStream.<anonymous> (/run_dir/repl.js:116:5)
    at ReadStream.emit (events.js:189:13)
    at addChunk (_stream_readable.js:284:12)
    at readableAddChunk (_stream_readable.js:265:11)
    at ReadStream.Readable.push (_stream_readable.js:220:10)
```

#### ES6 Affects on Scope and Hoisting

`var` - Does not provide block-scoping which is present in `let` and `const`.

```js
//Local 'var' Scope Example
function oldJsScopeVariable() {
	if (true) {
		var localVarVariable = "Local 'var' Variable";
	}
	console.log(localVarVariable);
}
```

The code above runs fine per the output below:

```console
>oldJsScopeVariable();

>
Local 'var' Variable
=> undefined
>
```

Many have different opinions about continuning the use of `var` moving forward. Personally I will not use unless a specific use case requires it simply for the sake of consistency.

`let` and `const` - Both provide block-scoping that is absent in the function-scoped `var` variable keyword.

## Hoisting

#### What is "Hoisting"?

> Hoisting - From MDN Reference
>
> > Hoisting is a term you will not find used in any normative specification prose prior to ECMAScript® 2015 Language Specification. Hoisting was thought up as a general way of thinking about how execution contexts (specifically the creation and execution phases) work in JavaScript. However, the concept can be a little confusing at first.
> >
> > Conceptually, for example, a strict definition of hoisting suggests that variable and function declarations are physically moved to the top of your code, but this is not in fact what happens. Instead, the variable and function declarations are put into memory during the compile phase, but stay exactly where you typed them in your code.

## _Only declarations are hoisted_

### **By declaring a variable and initializing it after using it, the variable will return undefined.**

### **If you initialize a variable before it is declared, it will return the value of the variable.**

## **Hoisting example using Python Tutor:**

<iframe width="560" height="315" src="https://www.youtube.com/embed/tip_1rrhIZQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Resources

https://developer.mozilla.org/en-US/docs/Glossary/Scope

https://scotch.io/tutorials/understanding-scope-in-javascript

https://developer.mozilla.org/en-US/docs/Glossary/Hoisting

[http://pythontutor.com/ - JavaScript Tutor - Visualize JavaScript code execution to learn JavaScript online](http://pythontutor.com/javascript.html#code=let%20globalLetVariable%20%3D%20%22Global%20'let'%20Variable%22%3B%0Afunction%20globalScopeVariable%28%29%20%7B%0A%20%20%20%20if%20%28true%29%20%7B%0A%20%20%20%20%20%20%20%20console.log%28globalLetVariable%29%3B%0A%20%20%20%20%7D%0A%7D%0A%0AglobalScopeVariable%28%29%3B&curInstr=0&mode=display&origin=opt-frontend.js&py=js&rawInputLstJSON=%5B%5D)
