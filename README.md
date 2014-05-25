url-router
================

> NOTE: [Does not actually work yet!](https://github.com/codemix/url-router/issues/1)

See the [component page](http://codemix.github.io/url-router) for more information.


# Usage



```html
<template is="url-router" pattern="/">
  <h1>This is the homepage</h1>
</template>

```

```html
<template is="url-router" pattern="/about-us">
  <h1>This is the about us page</h1>
</template>

```

```html
<template is="url-router" pattern="/pages/<page>">
  <h1>This is the {{page}} page</h1>
</template>

```



```html
<template is="url-router" pattern="/<controller>">
  <h1>This is the {{controller}} controller</h1>
</template>

```


```html
<template is="url-router" pattern="/<controller>/<action>">
  <h1>This is the {{action}} action on the {{controller}} controller</h1>
</template>

```


```html
<template is="url-router" pattern="/<controller>/<action>/<pk:\d+>">
  <h1>This is the {{action}} action on the {{controller}} controller, operating on item: {{pk}}</h1>
</template>

```

### Nesting


```html
<template is="url-router" pattern="/pages/<page>">
  <h1>This is the {{page}} page</h1>
  <a href="#info">More Info</a>
  <template is="url-router" pattern="#info">
    <h1>This is only active when the fragment is `#info`</h1>
  </template>
</template>

```
