# What

The idea is to create a comprehensive DNA.css file filled with all your
variables and you use only the DNA when building your APP so you're consistent
in everything you do.

## In a nutshell

The DNA.css File

```css
:root {
  --base: 4px;
  --main-color: fuchsia;
  --bg-color: whitesmoke;
  --copy-color: black;
}
```

So your components can look like this:

```css
body {
  background-color: var(--bg-color);
}
.button {
  background-color: var(--main-color);
}
.headline {
  color: var(--copy-color);
}
```

## Get Started

[Play around with it in codepen](https://codepen.io/lassediercks/pen/rYdjzm)

Or install our recommended dna.css in your project

```
npm install @kalispera/dna.css
yarn add @kalispera/dna.css
```

Or lint the rest of your project to prevent using something else than the
dns.css

https://github.com/kalispera/stylelint-config-dnacss

```
