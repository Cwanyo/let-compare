# let-compare

Deep comparison for detecting the changes in props for React.

## Installation

```
$ npm install let-compare --save
```

## Usage

Using ES5 syntax:

```js
const letCompare = require("let-compare");
```

or ES6 syntax:

```js
import letCompare from "let-compare";
```

## Example

```jsx
import React from "react";
import letCompare from "let-compare";

const Card = ({ children }) => {
  return <div>{children}</div>;
};

const arePropsEqual = (preProps, newProps) => {
  return letCompare(preProps, newProps);
};

export default React.memo(Card, arePropsEqual);
```
