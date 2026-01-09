# What is my vision?

### Samples:

```md
# Hello 
## Markdown
### Spice
```

```html
<h1>Hello</h1>
<h2>Markdown</h2>
<h3>Spice</h3>
```

---

```md
Trying separate dash

---
```

```html
<p>Trying separate dash</p>
<hr>
```

---

```md
Hello **Markdown** *Spice*
- easy
- fast
- configurable
```

```html
<p>Hello <b>Markdown</b> <i>Spice</i></p>
<ul>
  <li>ease</li>
  <li>fast</li>
  <li>configurable</li>
</ul>
```
Everything what is in pure markdown ^^

---

Variables
```md
Hello Markdown *Spice* - this is message for {{name}}

Hello Markdown *Spice* - this is message for {{name|"Cube"}}; __with placeholder__
```

```html
<p>Hello Markdown <i>Spice</i> - this is message for <span spice-var="name"></span></p>
<p>Hello Markdown <i>Spice</i> - this is message for <span spice-var="name">Cube</span>; <small>with placeholder</small></p>
<script>
var SPICE_GLOBAL = {};
SPICE_GLOBAL.vars = {...SPICE_GLOBAL.vars, ...{name: null}}
</script>
```

---

Blocks
```md
:block-name::
# Hello MDSpice
:::

---
```

```html
<div spice-block-name="block-name">
  <h1>Hello MDSpice</h1>
</div>
<hr>
```

Blocks-class
```md
:block-name:.red-sqrt.radius-10:
# Hello MDSpice
:::

---
```

```html
<div spice-block-name="block-name" class="red-sqrt radius-10">
  <h1>Hello MDSpice</h1>
</div>
<hr>
```

Templates [Block section]
```md
:block-name::?
# Hello MDSpice - {{name}}
---
"Nano & Kat" ~ {{author}}
:::

---
```

```html
<template>
<div spice-block-name="block-name" class="red-sqrt radius-10">
  <h1>Hello MDSpice - <span spice-var="name"></span></h1>
  <hr>
  <p>"Nano & Kat" ~ <span spice-var="author"></span></p>
</div>
</template>
<hr>
```

Templates logic [Block section]
```
Block as template -> 
-> json structure with template tag -> 
-> list all variables and set in json ->
-> create function to clone template and set with specific variables ->
```

Usage sample:
```
:banner::?
### {{title}}

---

{{description}}

"{{quote}}" ~ {{quote_author}}
:::


:banner(
title: Banner #1
description: Bla bla bla...
quote: Bla bla more
quote_author: meh...
)

:banner(
title: Banner #2
description: Bla bla bla sth more...
quote: Bla bla more pitu pitu
quote_author: qubo
)
```








