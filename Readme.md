![dna-design](http://lassediercks.github.io/dna-design/logo.svg)

**A concept to achieve dynamic consistency in web interfaces**


### What

Look at a brand, company or product. The higher level identity which makes us remember them is the DNA.
The DNA is made of:

 * Colors
 * Fonts
 * Spacings

This layer is underneath everything.

To achieve consistency we only use what is in the dna.


### How

In the web, we can utilize the power of css custom properties (Of course this is also possible with preprocessors but slightly more complicated).

In the [sample dna file](./dna.css) you'll notice a bunch of variables.
This specific file is tailored for a simple need and should only reflect how to structure such a file.
Most likely it won't fit your needs and you have to adapt it. That's the idea of this. Build your own DNA, define your DNA and make use of it.


### Get Started

This repo comes with a DNA reset that can be compared to usual CSS resets but builds on top of the sample DNA file.

[look at the DNA reset](./dna-reset.css)

For a quick start just download the [dna.css](./dna.css) and [dna-reset.css](./dna-reset.css) and link them inside your head-tag.


```html
<link rel="stylesheet" href="dna-reset.css">
<link rel="stylesheet" href="dna.css">
```

Next create your personal DNA you can adjust the dna.css or create a new one and link it below them.

```html
<link rel="stylesheet" href="dna-reset.css">
<link rel="stylesheet" href="dna.css">
<link rel="stylesheet" href="mybrand.css">
```


### Examples

A DNA-based button could look like this:

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
