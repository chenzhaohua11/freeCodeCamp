---
id: 587d7b84367417b2b2512b34
title: 使用 type of 检查变量的类型
challengeType: 1
forumTopicId: 18374
---

# --description--

可以使用`typeof`检查变量的数据结构或类型。在处理多种数据类型时，`typeof`会对调试很有帮助。如果想计算两数之和，但实际传入了一个字符串参数，则结果可能是错误的。类型错误可能隐藏在计算或函数调用中。当你以 JavaScript 对象（JSON）的形式访问和使用外部数据时尤其要小心。

下面是使用`typeof`的一些示例：

```js
console.log(typeof ""); // 输出 "string"
console.log(typeof 0); // 输出 "number"
console.log(typeof []); // 输出 "object"
console.log(typeof {}); // 输出 "object"
```

JavaScript 有六种原始（不可变）数据类型：`Boolean`,`Null`,`Undefined`,`Number`,`String`, 和`Symbol`（ES6 新增）和一种可变的数据类型：`Object`。注意，在 JavaScript 中，数组在本质上是一种对象

# --instructions--

添加两个`console.log()`语句来检查代码中的两个变量`seven`和`three`的 `typeof`值。

# --hints--

你应在两个`console.log()`语句中使用`typeof`来检查变量的类型。

```js
assert(code.match(/console\.log\(typeof[\( ].*\)?\)/g).length == 2);
```

你应使用`typeof`来检查变量`seven`的类型。

```js
assert(code.match(/typeof[\( ]seven\)?/g));
```

你应使用`typeof`来检查变量`three`的类型。

```js
assert(code.match(/typeof[\( ]three\)?/g));
```

# --solutions--
