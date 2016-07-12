Linters
=======

eslint
------

JavaScript linter

### Setup

`.eslintrc`

```json
{
  "extends": "eslint:recommended",
  "env": {},
  "globals": {}
}
```

### Rules

<http://eslint.org/docs/rules/>

### Ignore line

```js
console.log('foo'); // eslint-disable-line
```

jshint
------

JavaScript linter

### Rules

<http://jshint.com/docs/options/>

### Ignore line

```js
console.log('foo'); // jshint ignore:line
```
