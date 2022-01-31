# How to setup a sticky sidebar inside a grid context

[LINK](https://ishadeed.com/article/position-sticky-css-grid/)

1. HTML

```
<div class='grid'>
  <aside class='asideSection'>...</aside>
  <main class='mainSection'>...</main>
</div>
```

2. CSS

```
.grid {
  display: grid;
  grid-template-columns: 100px 1fr;
}

.asideSection {
  position: sticky;
  top: 0;
  align-self: start; // forces content to stick
}

.mainSection {
  display: block;
}

```
