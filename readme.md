# object-assign [![Build Status](https://travis-ci.org/sindresorhus/object-assign.svg?branch=master)](https://travis-ci.org/sindresorhus/object-assign)

> ES2015 [`Object.assign()`](http://www.2ality.com/2014/01/object-assign.html) [ponyfill](https://ponyfill.com)


## Use the built-in

Node.js 4 and up, as well as every evergreen browser (Chrome, Edge, Firefox, Opera, Safari),
support `Object.assign()` :tada:. If you target only those environments, then by all
means, use `Object.assign()` instead of this package.


## Install

```
$ npm install object-assign
```


## Usage

```js
const objectAssign = require('object-assign');

objectAssign({foo: 0}, {bar: 1});
//=> {foo: 0, bar: 1}

// multiple sources
objectAssign({foo: 0}, {bar: 1}, {baz: 2});
//=> {foo: 0, bar: 1, baz: 2}

// overwrites equal keys
objectAssign({foo: 0}, {foo: 1}, {foo: 2});
//=> {foo: 2}

// ignores null and undefined sources
objectAssign({foo: 0}, null, {bar: 1}, undefined);
//=> {foo: 0, bar: 1}
```


## API

### objectAssign(target, [source, ...])

Assigns enumerable own properties of `source` objects to the `target` object and returns the `target` object. Additional `source` objects will overwrite previous ones.


## Resources

- [ES2015 spec - Object.assign](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-object.assign)


---

<div align="center">
	<b>
		<a href="https://tidelift.com/subscription/pkg/npm-object-assign?utm_source=npm-object-assign&utm_medium=referral&utm_campaign=readme">Get professional support for this package with a Tidelift subscription</a>
	</b>
	<br>
	<sub>
		Tidelift helps make open source sustainable for maintainers while giving companies<br>assurances about security, maintenance, and licensing for their dependencies.
	</sub>
</div>
