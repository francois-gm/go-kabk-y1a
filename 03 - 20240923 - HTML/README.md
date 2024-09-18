# Class 3, 2024/09/23

## Intro

- A website you like (Matilde, Jeungin, François)

## Recap

- Name an example of a HTML `tag`?
- How would you define, in your own words, what does at HTML `tag` does?
- Name an example of a HTML `attribute`?
- How would you define, in your own words, what does at HTML `attribute` does?
- In an HTML document, what goes inside of the `<head>` tag?
- In an HTML document, what goes inside of the `<body>` tag?

## CSS

> What is CSS?

CSS stands for **C**ascade **S**tyle **S**heet.

1. It behaves in a **cascade**.

But what does that mean? It means that:

- You at first apply style rules that are general: they apply to all your elements, and are not very specific. As an example, all paragraphs have a blue color.
- The you apply style rules that are more specific. As an example, the paragraph with a red class has a red color. All other paragraphs will keep their blue color.
- Instead of naming every paragraph of your document and individually attributing them colors, you would say:
All paragraphs have a blue color, paragraphs with the red class has a red color.

2. It **styles** the HTML elements (it's like painting the HTML blocks).
3. It is a **sheet**.

### Principles of CSS:

- Precedence and priority (the cascade)
- Selectors types and granularity in selecting.
- The CSS **property-value** pair, as an example `color: blue;` where `color` is the property and `blue` is the value.
- Pseudo classes (`a:hover`) apply to specific states (when the mouse hovers the `<a>` element, this CSS rules applies).

#### Selectors

CSS selectors are used to “find” (or select) the HTML elements you want to style.

##### Simple selectors

- The **element** selector
  - In HTML: `<p>`
  - In CSS: `p{ property:value; }`
  - Not very specific, less CSS 'cascade points'.
- The **class** selector
  - In HTML: `<p class="my-class">`
  - In CSS: `p.my-class{ property:value; }`
  - More specific than an *element* selector, more CSS 'cascade points'.
  - You can have several elements sharing the same *class* in your HTML document.
- The **id** selector
  - In HTML: `<p id="my-id">`
  - In CSS: `p#my-id{ property:value; }`
  - More specific than a class selector, so even more CSS 'cascade points'.
  - An id is unique, meaning you can only use each id once per html document.

##### Combinator selectors

Select elements based on a specific relationship between them.

Example 1:

- `p.my-class a.my-other-class`
- Applies to `<a>` elements with the class `my-other-class` inside `<p>` elements with the class `my-class`
- More specific than simple selector, so even even more CSS cascade points. The more specific, the more points, the more 'deep' in the cascade, the more it has precedence over less specific CSS rules.

Example 2:

- `div.my-class p:first-of-type`
- Applies to the first `<p>` element inside a `<div>` element with the class `my-class`
- Again, more specific than simple selector, so even even more CSS cascade points. The more specific, the more points, the more 'deep' in the cascade, the more it has precedence over less specific CSS rules.


- [CSS Diner](https://flukeout.github.io)

Pseudo-class selectors (select elements based on a certain state)
Pseudo-elements selectors (select and style a part of an element)
Attribute selectors (select elements based on an attribute or attribute value)


d

###

- Presentation assignment 1

I do, we do, you do

