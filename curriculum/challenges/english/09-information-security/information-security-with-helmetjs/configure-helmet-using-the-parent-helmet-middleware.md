---
id: 587d8249367417b2b2512c40
title: Configure Helmet Using the ‘parent’ helmet() Middleware
challengeType: 2
forumTopicId: 301575
---

# --description--

As a reminder, this project is being built upon the following starter project on [Repl.it](https://repl.it/github/freeCodeCamp/boilerplate-infosec), or cloned from [GitHub](https://github.com/freeCodeCamp/boilerplate-infosec/).

`app.use(helmet())` will automatically include all the middleware introduced above, except `noCache()`, and `contentSecurityPolicy()`, but these can be enabled if necessary. You can also disable or configure any other middleware individually, using a configuration object.

<h3>Example:</h3>

```js
app.use(helmet({
  frameguard: {         // configure
    action: 'deny'
  },
  contentSecurityPolicy: {    // enable and configure
    directives: {
      defaultSrc: ["self"],
      styleSrc: ['style.com'],
    }
  },
  dnsPrefetchControl: false     // disable
}))
```

We introduced each middleware separately for teaching purposes and for ease of testing. Using the ‘parent’ `helmet()` middleware is easy to implement in a real project.

# --hints--

no tests - it's a descriptive challenge

```js
assert(true);
```

# --seed--

# --solutions--

```js
/**
  Backend challenges don't need solutions, 
  because they would need to be tested against a full working project. 
  Please check our contributing guidelines to learn more.
*/
```