---
id: 5900f3891000cf542c50fe9c
challengeType: 5
isHidden: false
title: 'Problem 29: Distinct powers'
forumTopicId: 301941
---

## Description
<section id='description'>

Consider all integer combinations of ab for 2 ≤ a ≤ 5 and 2 ≤ b ≤ 5:

<div style='padding-left: 4em;'>
  2<sup>2</sup>=4, 2<sup>3</sup>=8, 2<sup>4</sup>=16, 2<sup>5</sup>=32 <br>
  3<sup>2</sup>=9, 3<sup>3</sup>=27, 3<sup>4</sup>=81, 3<sup>5</sup>=243 <br>
  4<sup>2</sup>=16, 4<sup>3</sup>=64, 4<sup>4</sup>=256, 4<sup>5</sup>=1024 <br>
  5<sup>2</sup>=25, 5<sup>3</sup>=125, 5<sup>4</sup>=625, 5<sup>5</sup>=3125 <br>
</div>

If they are then placed in numerical order, with any repeats removed, we get the following sequence of 15 distinct terms:

<div style='padding-left: 4em;'>
  4, 8, 9, 16, 25, 27, 32, 64, 81, 125, 243, 256, 625, 1024, 3125
</div>

How many distinct terms are in the sequence generated by <var>a<sup>b</sup></var> for 2 ≤ <var>a</var> ≤ <var>`n`</var> and 2 ≤ <var>b</var> ≤ <var>`n`</var>?

</section>

## Instructions
<section id='instructions'>

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: <code>distinctPowers(15)</code> should return a number.
    testString: assert(typeof distinctPowers(15) === 'number');
  - text: <code>distinctPowers(15)</code> should return 177.
    testString: assert.strictEqual(distinctPowers(15), 177);
  - text: <code>distinctPowers(20)</code> should return 324.
    testString: assert.strictEqual(distinctPowers(20), 324);
  - text: <code>distinctPowers(25)</code> should return 519.
    testString: assert.strictEqual(distinctPowers(25), 519);
  - text: <code>distinctPowers(30)</code> should return 755.
    testString: assert.strictEqual(distinctPowers(30), 755);

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function distinctPowers(n) {
  // Good luck!
  return n;
}

distinctPowers(30);
```

</div>



</section>

## Solution
<section id='solution'>


```js
const distinctPowers = (n) => {
  let list = [];
  for (let a=2; a<=n; a++) {
    for (let b=2; b<=n; b++) {
      let term = Math.pow(a, b);
      if (list.indexOf(term)===-1) list.push(term);
    }
  }
  return list.length;
};
```

</section>