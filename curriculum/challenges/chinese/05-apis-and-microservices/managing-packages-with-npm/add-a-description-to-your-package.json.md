---
id: 587d7fb3367417b2b2512bfc
title: 给 package.json 添加一个描述
challengeType: 2
forumTopicId: 301522
---

# --description--

一个好的 package.json 文件的下一部分就是 description 字段，通过简洁的文字来描述你的项目。

如果你计划将来把这个包发布到 npm，请注意 description 字段的作用是告知用户这个包的用途，这样用户就可以决定是否要安装你发布的包。然而，这并不是描述信息的唯一使用场景：它也是一种很好的总结项目的方式，对于一个普通的 Node.js 项目来说，它可以帮助其它开发者、未来的维护者以及你自己快速地了解项目，这同样非常重要。

无论你如何计划项目，都建议你使用描述信息。我们来添加类似这样的信息：

```json
"description": "A project that does something awesome",
```

# --instructions--

在 Glitch 项目的 package.json 中添加描述。

请记住使用（"）包裹字段名并且使用（,）分隔字段。

# --hints--

package.json 应该有一个有效的 'description' 键。

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/package.json').then(
    (data) => {
      var packJson = JSON.parse(data);
      assert(packJson.description, '"description" is missing');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

# --solutions--
