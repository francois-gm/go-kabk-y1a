# Class 7, 2024/10/21

## Intro (15min)

- A website you like (Duru, Yoonjin, François)

## An *Ode to CSS*, each present their final project (1h)

### a) Put your website online (15min)

1) Create an account on [Netlify](https://app.netlify.com).
2) `Site` -> `Deploy manually` (`browse to upload`).
3) When browsing, select your *project* folder (`my-project-template`, as an example), by this I mean the **root** folder of your project, that contains your `index.html`, your `assets` and your `content` folders.
4) There it is!

Add your url to the list.

### b) Presentation

- You have **two minutes** to present the website of one of your classmate (so not your website).
- First, do a *test drive* of the website. *Click, resize, scroll*…
- **How does the website works?** Functionality? Aesthetics? Conceptual? **Describe it in a few sentences**.

Then:

- **Guess the CSS property** (class can help if not easy to guess, too).
- What does this project make you think of?
- Give a **positive quality** / something you **appreciate** in the website, and tell us **why**.
- Think of the challenges / difficulties of working with this CSS property? How was this addressed?
- If you would have to work on this website, are there elements you could either fine-tune or push further? Think functional, aesthetical, conceptual.

| Name | URL | Presented by |
| -- | -------------- | ------------- |
| Lucile | - | Amy |
| Sam | - | Lucile |
| Matilde | - | Sam |
| Jeungin | - | Matilde |
| Nell | - | Jeungin |
| Khulan | - | Nell |
| Timmy | - | Khulan |
| Fedja | - | Timmy |
| Duru | - | Fedja |
| Yoonjin | - | Duru |
| Kaja | - | Yoonjin |
| Max | - | Kaja |
| Yalizah | - | Max |
| Maria | - | Yalizah |
| Femke | - | Maria |
| Alexandr | - | Femke |
| Myrto | - | Alexandr |
| Andrei | - | Myrto |
| Olya | - | Andrei |
| Mani | - | Olya |
| Isaac | - | Manu |
| Amy | - | Isaac |

## Tutorial: Javascript essentials (30min)

- What does Javascript do?
  
- Essential terminology:
  
  - What is [a variable](https://www.w3schools.com/js/js_variables.asp) and [data types](https://www.w3schools.com/js/js_datatypes.asp)?
  - What is [an event](https://www.javatpoint.com/javascript-events) (event handler with [addEventListener](https://www.w3schools.com/jsref/met_document_addeventlistener.asp))?
  - What is a [function](https://www.w3schools.com/js/js_functions.asp)?
  - What is a [conditional statement](https://www.w3schools.com/js/js_comparisons.asp)?
  - What are javascript [expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators) and [operators](https://www.w3schools.com/js/js_operators.asp)?

Variables:

`var`, is a variable
`let`, is a variable that can be redefined (**let** this be this value).
`const`, is a variable that is not redefined (this value is **const**ant).

```
var appleCount = 5;
var orangeCount = 5;
var lemonCount = 2;
var bananaCount = 3;

const appleColor = "red";

let fruitCount = appleCount + orangeCount + lemonCount + bananaCount;
```
where `fruitCount` equals to **15**.
```
let citrusCount = orangeCount + lemonCount;
```
where `citrusCount` equals to **7**.

Comparison operators

- `>` is bigger than
- `<` is smaller than
- `>=` is bigger or equal to
- `<=` is smaller or equal to
- `==` is equal to
- `!=` is not equal to
- `===` is strictly equal to
- `!==` is strictly not equal to

Logical operators

- `&&` and
- `||` or

```
let juiceType;

if( (lemonCount > 0) && (orangeCount < 1) ){
  let juiceType = lemonade;
else if ( (lemonCount > 0) && (orangeCount > 0) ){
  let juiceType = citrusPunch;
else{
  let juiceType = fruitPunch
}
```

## Tutorial: manipulating the document (the *DOM*) with Javascript (2h)

- We create basic JS event handlers (on click, on mouse over, on scroll)
- We create a toggler button (dark mode, and or a modal menu)
- We create a JS counter (increment)
- We create a randomizer (shows random sentences on click)

## Pseudo-code examples

Look at [Pseudo-code](https://en.wikipedia.org/wiki/Pseudocode), [Structured English](https://en.wikipedia.org/wiki/Structured_English), [Natural-language programming](https://en.wikipedia.org/wiki/Natural-language_programming), [esoteric language](https://en.wikipedia.org/wiki/Esoteric_programming_language) (2h)
