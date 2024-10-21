# Class 7, 2024/10/21

## Intro (20min)

- A website you like (Duru, Yoonjin, François)

**About next class's (Monday November 4th) workshop…**

- Guess tutor class with [Clara Pasteau](https://www.clarapasteau.com).
- Clara will do a lunch lecture/presentation of her work (12h45-13h30) before that class, 1-2 students to create a visual for that (?)

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
| Lucile | https://aaaaaahhhblocksblocks.netlify.app | Amy |
| Sam | https://chipper-zabaione-ff4be2.netlify.app/ | Lucile |
| Matilde | https://boxshadoweddogs.netlify.app | Sam |
| Jeungin | https://unrivaled-cannoli-9d329d.netlify.app | Matilde |
| Nell | https://singular-yeot-592cd8.netlify.app/ | Jeungin |
| Khulan | https://profound-kitten-111905.netlify.app/ | Nell |
| Timmy | https://thewonderfulworldofborders.netlify.app | Khulan |
| Fedja | https://glistening-sprite-5892fb.netlify.app/ | Timmy |
| Duru | https://chic-salmiakki-b981be.netlify.app | Fedja |
| Yoonjin | https://venerable-cactus-314c19.netlify.app | Duru |
| Kaja | https://off-with-their-heads.netlify.app/ | Yoonjin |
| Max | https://playful-crostata-3b3249.netlify.app/ | Kaja |
| Yalizah | https://melodious-duckanoo-cfe379.netlify.app/ | Max |
| Maria | https://jolly-snickerdoodle-ec3788.netlify.app/ | Yalizah |
| Femke | https://rococo-eclair-ad8e97.netlify.app | Maria |
| Alexandr | https://sage-puffpuff-45545e.netlify.app/ | Femke |
| Myrto | https://timely-moonbeam-d148e6.netlify.app/ | Alexandr |
| Andrei | https://unreadable-andrei.netlify.app/ | Myrto |
| Olya | https://regal-souffle-a33a60.netlify.app/ | Andrei |
| Mani | https://thunderous-belekoy-91de20.netlify.app | Olya |
| Isaac | https://moonlit-nasturtium-8bb8de.netlify.app/ | Manu |
| Amy | https://timely-arithmetic-f3414d.netlify.app/ | Isaac |

## Tutorial: Javascript essentials (30min)

What does Javascript do?
  
Essential terminology:
  
  - What is [a variable](https://www.w3schools.com/js/js_variables.asp) and [data types](https://www.w3schools.com/js/js_datatypes.asp)?
  - What is [an event](https://www.javatpoint.com/javascript-events) (event handler with [addEventListener](https://www.w3schools.com/jsref/met_document_addeventlistener.asp))?
  - What is a [function](https://www.w3schools.com/js/js_functions.asp)?
  - What is a [conditional statement](https://www.w3schools.com/js/js_comparisons.asp)?
  - What are javascript [expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_operators) and [operators](https://www.w3schools.com/js/js_operators.asp)?

### Variables

*Variables are "containers" for storing data*

- `var`, is a variable declaration type
- `let`, is a variable declaration type that can be redefined (**let** this be this value).
- `const`, is a variable declaration type that is not redefined (this value is **const**ant).

*Data can be of several types*

- Boolean: `true` or `false`
- Number: `0`, `1`, `2`, `-1`, `-2`, `3.1416`
- String: `"someText"`
- Array: `["apple", "orange", "banana"]`
- Object: …

**Example**

```
let appleCount = 5;
let orangeCount = 5;
let lemonCount = 2;
let bananaCount = 3;

const appleColor = "red";
```
where the apple count **can change** but its color is always (**const**antly) red.
```
let fruitCount = appleCount + orangeCount + lemonCount + bananaCount;
```
where `fruitCount` equals to **15**.
```
let citrusCount = orangeCount + lemonCount;
```
where `citrusCount` equals to **7**.

### Events and functions

*A JavaScript **function** is a block of code designed to perform a particular task. A JavaScript function is executed when "something" invokes it (calls it, an **event** as an example)*

```
function myFunction() {
  document.getElementById("demo").innerHTML = "Hello World";
}
```
where above is the function and below is an event that invokes the function
```
document.addEventListener("click", myFunction);
```

### Expressions

*In JavaScript, an expression is a valid unit of code that resolves to a value*

- `5 + 3` produces 8
- `50 * 2` produces 100
- `"myText"` produces "myText"

### Operators

**Comparison operators**

- `>` is bigger than
- `<` is smaller than
- `>=` is bigger or equal to
- `<=` is smaller or equal to
- `==` is equal to
- `!=` is not equal to
- `===` is strictly equal to
- `!==` is strictly not equal to

**Logical operators**

- `&&` and
- `||` or

**Example of a conditional statement**

```
let juiceType;

if( (lemonCount >= 0) && (orangeCount == 0) ){
  juiceType = lemonade;
else if ( (lemonCount >= 0) && (orangeCount >= 0) ){
  juiceType = citrusPunch;
else{
  juiceType = fruitPunch;
}
```

- First we declare (but we don't define) the juice type.
- Then we ask if the lemon count is equal or over one, and there are no oranges.
- If that is the case, our juice type is a lemonade.
- If that is not the case, then (else if) we ask if the lemon count is equal or over one, and there is one orange or more.
- If that is the case, our juice is a citrus punch.
- If it's not a lemonade or a citrus punch, then it's a fruit punch.

## Tutorial: manipulating the document (the *DOM*) with Javascript (2h)

Ideas:

- Create a JS counter (increment)
- Create a JS random color generator
- Create a toggler button (dark mode, and or a modal menu)

## Pseudo-code examples

Look at [Pseudo-code](https://en.wikipedia.org/wiki/Pseudocode), [Structured English](https://en.wikipedia.org/wiki/Structured_English), [Natural-language programming](https://en.wikipedia.org/wiki/Natural-language_programming), [esoteric language](https://en.wikipedia.org/wiki/Esoteric_programming_language) (2h)
