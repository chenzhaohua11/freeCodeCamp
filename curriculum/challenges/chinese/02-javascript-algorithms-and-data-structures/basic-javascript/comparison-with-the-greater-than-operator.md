---
id: 56533eb9ac21ba0edf2244d4
title: 大于运算符
challengeType: 1
videoUrl: 'https://scrimba.com/c/cp6GbH4'
forumTopicId: 16786
---

# --description--

使用大于运算符（`>`）来比较两个数字。如果大于运算符左边的数字大于右边的数字，将会返回`true`。否则，它返回`false`。

与相等运算符一样，大于运算符在比较的时候，会转换值的数据类型。

**例如**

```js
5   >  3   // true
7   > '3'  // true
2   >  3   // false
'1' >  9   // false
```

# --instructions--

添加`大于`运算符到指定的行，使得返回的语句是有意义的。

# --hints--

`testGreaterThan(0)`应该返回 "10 or Under"。

```js
assert(testGreaterThan(0) === '10 or Under');
```

`testGreaterThan(10)`应该返回 "10 or Under"。

```js
assert(testGreaterThan(10) === '10 or Under');
```

`testGreaterThan(11)`应该返回 "Over 10"。

```js
assert(testGreaterThan(11) === 'Over 10');
```

`testGreaterThan(99)`应该返回 "Over 10"。

```js
assert(testGreaterThan(99) === 'Over 10');
```

`testGreaterThan(100)`应该返回 "Over 10"。

```js
assert(testGreaterThan(100) === 'Over 10');
```

`testGreaterThan(101)`应该返回 "Over 100"。

```js
assert(testGreaterThan(101) === 'Over 100');
```

`testGreaterThan(150)`应该返回 "Over 100"。

```js
assert(testGreaterThan(150) === 'Over 100');
```

你应该使用`>`运算符至少两次。

```js
assert(code.match(/val\s*>\s*('|")*\d+('|")*/g).length > 1);
```

# --solutions--
