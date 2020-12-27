---
id: 594db4d0dedb4c06a2a4cefd
title: 巴贝奇问题
challengeType: 5
videoUrl: ''
---

# --description--

<p> <a href='https://en.wikipedia.org/wiki/Charles_Babbage' title='wp：Charles_Babbage'>Charles Babbage</a> ，展望他的分析引擎能解决的各种问题，给出了这个例子： </p><blockquote>什么是正方形以数字269,696结尾的最小正整数？ </blockquote><p> - 巴贝奇，致鲍登勋爵的信，1837年;见Hollingdale和Tootill， <i>电子计算机</i> ，第二版，1970年，p。 125。 </p><p>他认为答案可能是99,736，其平方是9,947,269,696;但他无法确定。 </p><p>任务是找出巴贝奇是否有正确的答案。 </p><p>实现一个函数来返回满足Babbage问题的最小整数。如果巴贝奇是对的，返回巴贝奇的号码。 </p>

# --hints--

`babbage`是一种功能。

```js
assert(typeof babbage === 'function');
```

`babbage(99736, 269696)`不应该返回99736（答案较小）。

```js
assert.equal(babbage(babbageAns, endDigits), answer);
```

# --solutions--
