---
id: 5a24c314108439a4d4036176
title: 使用 State 切换元素
challengeType: 6
forumTopicId: 301421
---

# --description--

有时可能在更新状态的时候想知道上一个状态是什么。但是状态更新是异步的，这意味着 React 可能会把多个 `setState()` 集中在一起批量更新。所以设置 `this.state` 或者 `this.props` 后值没有立即更新。所以最好不要写如下的代码：

```js
this.setState({
  counter: this.state.counter + this.props.increment
});
```

正确的做法是，给 `setState` 传入一个函数，这个函数可以访问 state 和 props。给 `setState` 传入函数可以返回赋值后的 state 和 props。代码可以重写为这样：

```js
this.setState((state, props) => ({
  counter: state.counter + props.increment
}));
```

如果只需要 `state`，那么用下面的格式也是可以的：

```js
this.setState(state => ({
  counter: state.counter + 1
}));
```

注意一定要把 object 放在括号里，否则 JavaScript 会认为这只是代码片段。

# --instructions--

`MyComponent`有一个初始值为`false`的`visibility`属性。如果`visibility`的值为 true，render 方法返回一个视图，如果为 false，返回另一个视图。

目前，无法更新组件的`state`中的`visibility`属性，该值应在 true 和 false 之间来回切换。按钮上有一个单击处理程序，它触发一个名为`toggleVisibility()`的类方法。定义此方法，以便`visibility`的`state`在调用方法时切换到相反的值。如果`visibility`是`false`，则该方法将其设置为`true`，反之亦然。

最后，单击按钮以查看基于其`state`的组件的条件渲染。

**提示：** 不要忘记将`this`关键字绑定到构造函数中的方法上！

# --hints--

`MyComponent`应该返回一个`div`元素，其中包含一个`button`元素。

```js
assert.strictEqual(
  Enzyme.mount(React.createElement(MyComponent)).find('div').find('button')
    .length,
  1
);
```

`MyComponent`应该使用设置为`false`的`visibility`属性来初始化其 state。

```js
assert.strictEqual(
  Enzyme.mount(React.createElement(MyComponent)).state('visibility'),
  false
);
```

单击按钮元素应在`true`和`false`之间切换`visibility`属性的状态。

```js
async () => {
  const waitForIt = (fn) =>
    new Promise((resolve, reject) => setTimeout(() => resolve(fn()), 250));
  const mockedComponent = Enzyme.mount(React.createElement(MyComponent));
  const first = () => {
    mockedComponent.setState({ visibility: false });
    return waitForIt(() => mockedComponent.state('visibility'));
  };
  const second = () => {
    mockedComponent.find('button').simulate('click');
    return waitForIt(() => mockedComponent.state('visibility'));
  };
  const third = () => {
    mockedComponent.find('button').simulate('click');
    return waitForIt(() => mockedComponent.state('visibility'));
  };
  const firstValue = await first();
  const secondValue = await second();
  const thirdValue = await third();
  assert(!firstValue && secondValue && !thirdValue);
};
```

应该传入`setState` 一个匿名函数。

```js
const paramRegex = '[a-zA-Z$_]\\w*(,[a-zA-Z$_]\\w*)?';
const noSpaces = code.replace(/\s/g, '');
assert(
  new RegExp(
    'this\\.setState\\((function\\(' +
      paramRegex +
      '\\){|([a-zA-Z$_]\\w*|\\(' +
      paramRegex +
      '\\))=>)'
  ).test(noSpaces)
);
```

不要在 `setState` 里面使用 `this`。

```js
assert(!/this\.setState\([^}]*this/.test(code));
```

# --solutions--
