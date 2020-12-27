---
id: 9d7123c8c441eeafaeb5bdef
title: 使用 slice 而不是 splice 从数组中移除元素
challengeType: 1
forumTopicId: 301236
---

# --description--

使用数组时经常遇到要删除一些元素并保留数组剩余部分的情况。为此，JavaScript 提供了`splice`方法，它接收两个参数：从哪里开始删除项目的索引，和要删除的项目数。如果没有提供第二个参数，默认情况下是移除到结尾的元素。但`splice`方法会改变调用它的原始数组。举个例子：

```js
var cities = ["Chicago", "Delhi", "Islamabad", "London", "Berlin"];
cities.splice(3, 1); // Returns "London" and deletes it from the cities array
// cities is now ["Chicago", "Delhi", "Islamabad", "Berlin"]
```

正如我们在上一次挑战中看到的那样，`slice`方法不会改变原始数组，而是返回一个可以保存到变量中的新数组。回想一下，`slice`方法接收两个参数，从开始索引开始选取到结束（不包括该元素），并在新数组中返回这些元素。使用`slice`方法替代`splice`有助于避免数组变化产生的副作用。

# --instructions--

用`slice`代替`splice`重写`nonMutatingSplice`函数。将`cities`数组长度限制为3，并返回一个仅包含前 3 项的新数组。

不要改变提供给函数的原始数组。

# --hints--

应该使用`slice`方法。

```js
assert(code.match(/\.slice/g));
```

不能使用`splice`方法。

```js
assert(!code.match(/\.splice/g));
```

不能改变`inputCities`数组。

```js
assert(
  JSON.stringify(inputCities) ===
    JSON.stringify(['Chicago', 'Delhi', 'Islamabad', 'London', 'Berlin'])
);
```

`nonMutatingSplice(['Chicago', 'Delhi', 'Islamabad', 'London', 'Berlin'])`应返回`['Chicago', 'Delhi', 'Islamabad']`。

```js
assert(
  JSON.stringify(
    nonMutatingSplice(['Chicago', 'Delhi', 'Islamabad', 'London', 'Berlin'])
  ) === JSON.stringify(['Chicago', 'Delhi', 'Islamabad'])
);
```

# --solutions--
