---
id: 5a24c314108439a4d403614c
title: 从 Redux Store 获取状态
challengeType: 6
forumTopicId: 301443
---

# --description--

Redux store 对象提供了几种允许你与之交互的方法，你可以使用`getState()`方法检索 Redux store 对象中保存的当前的`state`。

# --instructions--

在代码编辑器中可以将上一个挑战中的代码更简洁地重写，在`store`中使用`store.getState()`检索`state`，并将其分配给新变量`currentState`。

# --hints--

redux store 的 state 应该有一个初始值 5。

```js
assert(store.getState() === 5);
```

应该存在一个变量`currentState`，并为其分配 Redux store 的当前状态。

```js
(getUserInput) =>
  assert(
    currentState === 5 && getUserInput('index').includes('store.getState()')
  );
```

# --solutions--
