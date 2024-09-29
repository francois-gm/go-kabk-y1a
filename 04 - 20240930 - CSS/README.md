# Class 4, 2024/09/30

## Intro (30min)

- A website you like (Nell, Khulan, François)

## Recap (15min)

- Why would one wants to add `CSS` in their `HTML` document?
- Name three places where you can add your CSS in your document. Where would it be, preferably?
- What is the "cascade"?
- *I want to write a `CSS` selector to target an `HTML` element so I can style it...*
  - Name a **general** way of selecting that element
  - Name a **more specific** way of selecting that element (using **one** HTML `attribute`)
  - Name a **very specific** way to selecting that element (using **one** HTML `attribute`)
- **True** or **false**...
  - When writing a `CSS` selector, you can combine different `class` under one selector.
  - When writing a `CSS` selector, you can combine diffrent `id` under one selector.
  - You can give multiple `id` values to one `HTML` element.
  - Each HTML element needs to have its individual selector in order to be *styled* by CSS.
  - **General** `CSS` selector are **more important** than **specific ones** (and their styling overwrite specific ones).
- **Name three** examples of CSS properties and **what** they visually do.

Bonus:

- What was the most **common** coding "issue" experienced during our last class (guess: it's not really a ~~coding~~ mistake)?
  
## Tutorial: extending on CSS selectors (15min)

Last class, we saw several ways of writing *CSS selectors* to style our HTML elements.

In short: The more the combination is specific, the more it has 'cascade points' and the more it has precedence over other CSS rules.

But how does the 'CSS algorithm' actually works?

<img src="css-specificity.svg" width="600px">

- Inline CSS = 1-0-0-0
- Id = 0-1-0-0 (added for each in a matching selector)
- Class, pseudo-class, attribute = 0-0-1-0 (added for each in a matching selector)
- Element, pseudo-element, 0-0-0-1 (added for each in a matching selector)

## Exercise 1, HTML/CSS selector based on specificity (30min)

You are assigned with a *specificity* value.

1. Define a CSS selector that matches with the assigned value.

| Specificity | Name |
| --------  | --------------------- |
| 0-0-0-1 | Lucile, Matilde |
| 0-0-0-3 | Sam, Jeungin |
| 0-0-1-1 | Nell, Timmy |
| 0-0-1-2 | Khulan, Fedja |
| 0-0-2-1 | Duru, Kaja |
| 0-0-2-3 | Yoonjin, Max |
| 0-0-4-2 | Yalizah, Alexandr |
| 0-1-0-1 | Femke, Olya |
| 0-1-2-3 | Maria, Isaac |
| 0-2-1-0 | Mani, Amy |
| 0-2-3-2 | Myrto, Andrei |

2. Exchange your CSS selector with someone. Now, write the HTML markup that corresponds to the selector you received.
3. To make sure that the selector targets the HTML element you wrote, give that selector some CSS properties/values (the `color` or `background-color` properties as examples).

## Tutorial: more CSS (1h)

- display, position, float.
- width, height.
- flexbox.
- 
- Inside your project folder, you have an html file named `index.html`.
- Inside your project folder, you have a subfolder called `assets`, and in that folder, you have a subfolder for your `CSS`, and one for your `Javascript`.
- Inside your `css` subfolder you have your `style.css` file.
- Inside your `js` subfolder you have your `script.js` file.

```
your-project-folder

   ├── index.html
   ├── content
   └── assets
       ├── css
       │   └── style.css
       └── js
           └── script.js
```

You link your style.css and script.js files in your html document.

For `style.css`:

- For the `style.css` document, this should be inside the <head> of your html document.
- `<link rel="stylesheet" href="assets/css/style.css">`

For `script.js`:

- For the `script.js` document, this should be at the end of your html document.
- `<script src="assets/js/script.js"></script>`

## Tutorial: CSS (1h)

> What is CSS?

CSS stands for **C**ascade **S**tyle **S**heet.

1. It behaves like a **cascade**.
2. It **styles** the HTML elements (it's like painting the HTML blocks).
3. It is a **sheet**.
   
But what does **behaves like a cascade** means? It means that:

- You at first apply style rules that are general: they apply to all your elements, and are not very specific. As an example, **all paragraphs** have a **blue color**.
- The you apply style rules that are more specific. As an example, **the paragraph with a red class** has a **red color**. All other paragraphs will keep their blue color.
- In summary: All paragraphs have a blue color, paragraphs with the red class has a red color.

```
p{
  color:blue;
}

p.red{
  color:red;
}
```

## Principles of CSS:

- Precedence and priority (the cascade)
- Selectors types and granularity in selecting.
- The CSS **property-value** pair, as an example `color: blue;` where `color` is the property and `blue` is the value.
- Pseudo classes (`a:hover`) apply to specific states (when the mouse hovers the `<a>` element, this CSS rules applies).

<img src="css-terminology.svg" width="750px">

### Selectors

CSS selectors are used to “find” (or select) the HTML elements you want to style.

#### Simple selectors

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

#### Combinator selectors

Select elements based on a specific relationship between them.

Example 1:

- `p.my-class a.my-other-class`
- Applies to `<a>` elements with the class `"my-other-class"` inside `<p>` elements with the class `"my-class"`
- More specific than simple selector, so even even more CSS cascade points. The more specific, the more points, the more 'deep' in the cascade, the more it has precedence over less specific CSS rules.

Example 2:

- `div.my-class p:first-of-type`
- Applies to the first `<p>` element inside a `<div>` element with the class `"my-class"`
- Again, more specific than simple selector, so even even more CSS cascade points. The more specific, the more points, the more 'deep' in the cascade, the more it has precedence over less specific CSS rules.

In example 2, we also have a **pseudo-class** selector, the `:first-of-type` selector.

> A CSS pseudo-class is a keyword added to a selector that specifies a special state of the selected element(s).

[Read more about pseudo-class selectors on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

In short: The more the combination is specific, the more it has 'cascade points' and the more it has precedence over other CSS rules.

<img src="css-specificity.svg" width="600px">

- Inline CSS = 1-0-0-0
- Id = 0-1-0-0 (added for each in a matching selector)
- Class, pseudo-class, attribute = 0-0-1-0 (added for each in a matching selector)
- Element, pseudo-element, 0-0-0-1 (added for each in a matching selector)

## Read more

- [All CSS selectors on W3school](https://www.w3schools.com/cssref/css_selectors.php)
- [CSS selectors on web.dev](https://web.dev/learn/css/selectors?hl=en)
- [More about how specificity gets calculated](https://webdesign.tutsplus.com/what-is-css-specificity--cms-34141t)
- [Visual examples on specificity](https://www.w3schools.com/cssref/trysel.php?)
- Practice your selectors by [playing the CSS Diner](https://flukeout.github.io) game!
- ... or play [this other game](https://toolness.github.io/css-selector-game/)
  
## CSS *properties* and *values*

*A CSS property determines an HTML element's style or behavior. Examples include font style, transform, border, color, and margin.*

- [CSS properties almanac on CSS tricks.com](https://css-tricks.com/almanac/properties/)
- [Basic CSS properties on simmons.edu](http://web.simmons.edu/~grabiner/comm244/weekthree/css-basic-properties.html)
- [All CSS properties on W3school](https://www.w3schools.com/cssref/index.php)
- [CSS tutorial W3school](https://www.w3schools.com/css/default.asp)

## Exercise 3 (15min)

- Complete levels 1-15 on [the CSS Diner](https://flukeout.github.io).
- Then we will do them together.

## Exercise 4, HTML/CSS selector based on specificity (30min)

You are assigned with a *specificity* value.

1. Write a CSS selector that matches with the assigned value.

| Specificity | Name |
| --------  | --------------------- |
| 0-0-0-1 | Lucile, Matilde |
| 0-0-0-3 | Sam, Jeungin |
| 0-0-1-1 | Nell, Timmy |
| 0-0-1-2 | Khulan, Fedja |
| 0-0-2-1 | Duru, Kaja |
| 0-0-2-3 | Yoonjin, Max |
| 0-0-4-2 | Yalizah, Alexandr |
| 0-1-0-1 | Femke, Olya |
| 0-1-2-3 | Maria, Isaac |
| 0-2-1-0 | Mani, Amy |
| 0-2-3-2 | Myrto, Andrei |

2. Exchange your CSS selector with someone. Now, write the HTML markup that corresponds to the selector you received.
3. To make sure that the selector targets the HTML element you wrote, give that selector some CSS properties/values (the `color` or `background-color` properties as examples).

## Presentation assignment 1

[See dedicated page](https://github.com/francois-gm/go-kabk-y1a/tree/main/03%20-%20Assignment%201%20(ode%20to%20CSS))