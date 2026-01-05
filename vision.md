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
