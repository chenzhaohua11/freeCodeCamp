---
id: cf1111c1c11feddfaeb7bdef
title: Nest one Array within Another Array
challengeType: 1
videoUrl: 'https://scrimba.com/c/crZQZf8'
forumTopicId: 18247
---

# --description--

You can also nest arrays within other arrays, like below:

```js
[["Bulls", 23], ["White Sox", 45]]
```

This is also called a <dfn>multi-dimensional array<dfn>.</dfn></dfn>

# --instructions--

Create a nested array called `myArray`.

# --hints--

`myArray` should have at least one array nested within another array.

```js
assert(Array.isArray(myArray) && myArray.some(Array.isArray));
```

# --seed--

## --after-user-code--

```js
if(typeof myArray !== "undefined"){(function(){return myArray;})();}
```

## --seed-contents--

```js
// Only change code below this line
var myArray = [];
```

# --solutions--

```js
var myArray = [[1,2,3]];
```