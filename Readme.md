# Dna Design
When our components are atomic, our idendity is the Dna.

Dna Design is a approach how to structure variable files.

### Why

We're heading into a direction where our code reflects the single source of truth for our Design.
The identity of a Brand, Company or Person is stored in a single source of truth file which is the dna of your brand.

If you decide to change that dna, the website will adapt.


### How

The most significant aspects of a dna are colors, your font-family and spacings.


```css
--font-family: sans-serif;
--dark: black;
--light: white;
--main-color: fuchsia;

--base: 4px;
```

Dna design starts to shine because these first variables get applied on the next level

```css

--bg-color: var(--light);
--copy-color: var(--dark);
--content-width: calc(var(--base)*175);

```

This repo comes with a dna reset that can be seen as a usual css reset. Compared to other css resets it's assumes you have dna file in places and resets html to your dna.

[look at the dna reset](./dna-reset.css)


### Where to start

When you want to build your website on top of a design dna, it's important to understand that the idea is that you don't define new dna aspect somewhere else.

For a quick start, just download the [dna.css](./dna.css) and [dna-reset.css](./dna-reset.css) and link them in your head.


```html
<link rel="stylesheet" href="dna-reset.css">
<link rel="stylesheet" href="dna.css">
```

After that, create your personal dna file and position them below them.


```html
<link rel="stylesheet" href="dna-reset.css">
<link rel="stylesheet" href="dna.css">
<link rel="stylesheet" href="mybrand.css">
```


After that, you're ready to head straight into your website creation.

A DNA based button for example could look like this:

```css

.button{
  cursor: pointer;
  text-decoration: none;
  font-weight: var(--font-weight);
  box-sizing: border-box;
  font-family: var(--font-family);
  background: var(--main-color);
  white-space: nowrap;
  padding: 0 var(--inner-x);
  margin-bottom: var(--outer-y);
  font-size: var(--font-size--S);
  height: var(--size--M);
  border-radius: var(--border-radius);
  color: var(--light);

  transition: box-shadow var(--fast) ease-in-out;
}
```

And a Hero area could look like this:

```css

.hero-area{
  background-color: var(--main-color);
  color: var(--light);
}
```
As you have the knowledge about your main color, your have to decide if the color in the hero area is light or dark.
