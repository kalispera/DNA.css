# DNA Design
When our components are atomic, our identity is the DNA.

DNA Design is a approach how to structure variable files.

### Why

We're heading into a direction where our code reflects the single source of truth for our design.
The identity of a brand, company or person is stored in a single source of truth file which is the DNA of your brand.

If you decide to change the DNA - the website will adapt.


### How

The most significant aspect of a DNA are colors, your font-family and spacings.


```css
--font-family: sans-serif;
--dark: black;
--light: white;
--main-color: fuchsia;

--base: 4px;
```

DNA design starts to shine because these first variables get applied on the next level

```css

--bg-color: var(--light);
--copy-color: var(--dark);
--content-width: calc(var(--base)*175);

```

This repo comes with a dna reset that can be seen as a usual CSS reset. Compared to other CSS resets it assumes you have a DNA file in places and resets the html to your DNA.

[look at the dna reset](./dna-reset.css)


### Where to start

When you want to build your website on top of a design DNA, it's important to understand that the point is to not define new DNA aspects somewhere else.

For a quick start just download the [dna.css](./dna.css) and [dna-reset.css](./dna-reset.css) and link them inside your head-tag.


```html
<link rel="stylesheet" href="dna-reset.css">
<link rel="stylesheet" href="dna.css">
```

Next create your personal dna file and link them below.

```html
<link rel="stylesheet" href="dna-reset.css">
<link rel="stylesheet" href="dna.css">
<link rel="stylesheet" href="mybrand.css">
```


After that you're ready to head straight into your website creation.

For example a DNA-based button could look like this:

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

And a hero area could look like this:

```css

.hero-area{
  background-color: var(--main-color);
  color: var(--light);
}
```
Because you have the knowledge about your main color, you have to decide if the color in the hero area is light or dark.
