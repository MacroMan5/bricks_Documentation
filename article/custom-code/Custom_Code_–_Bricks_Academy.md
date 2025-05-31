# Custom Code – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/custom-code/](https://academy.bricksbuilder.io/article/custom-code/)  
**Last Updated:** 2025-05-22T19:59:26.600Z  
**Extracted:** 2025-05-31 16:56:43

---

# Custom Code – Bricks Academy

Bricks allows you to add your own custom code (CSS, JavaScript, HTML, PHP) to various parts of your website.

How To Add Custom Code in Bricks (CSS, JS, HTML, PHP) - YouTube

[](https://www.youtube.com/watch?v=LiYwBZ_R-f8&embeds_referring_euri=https%3A%2F%2Facademy.bricksbuilder.io%2F)

## Global CSS & JavaScript

You can add your own **Custom CSS** & **Custom JavaScript** globally from your WordPress dashboard under **Bricks > Settings > Custom Code**.

Custom scripts (JavaScript) can be added in three different (document) locations:

*   **Header scripts**: Adds your scripts right before the closing </head> tag. This is where you want to copy & paste tracking scripts, etc.
*   **Body (header) scripts**: Adds your scripts right after the opening <body> tag.
*   **Body (footer) scripts**: Adds your scripts right before the closing </body> tag.

## Page-Specific CSS & JavaScript

To apply custom CSS & JavaScript to a specific page, edit this page with Bricks. Go to **Settings > Page Settings > Custom Code**. There, you can add your custom CSS & JS that should only be applied to the page you are currently editing.

## Element-Specific Custom CSS

![](https://academy.bricksbuilder.io/wp-content/uploads/2023/09/bricks-1.9.1-custom-css-root-placeholder-591x1024.png)

Extend the styles of any element and global class by adding your own custom CSS to it.

First, edit the element to which you want to add your own custom CSS.

Under the “Style” tab, open the “CSS” control group.

There, you can find the **Custom CSS** code editor. 

Use the `**%root%**` placeholder to target the element or global class you are currently editing. Bricks automatically converts this**`**%root%**`** placeholder to your element ID or global class.

Keyboard shortcode to insert **`**%root%**`** is “r + TAB”.

The screenshot on the right illustrates how to add a 1px width red border to an element.

### CSS code completion via Emmet

You can use CSS abbreviations to write your CSS even faster. Instead of writing `margin: 10px`, simply type `m10` and press the TAB key.

[https://docs.emmet.io/css-abbreviations/](https://docs.emmet.io/css-abbreviations/)

## Code Element (PHP, HTML, CSS, JS)

The “Code” element allows you to execute your own code (PHP, HTML, CSS & JS) anywhere on any page.

By default, the code added to the Code element is displayed as a code snippet.

In order to execute your code, you need to first enable **“Code Execution”** for the appropriate user role or user in your WordPress dashboard under “Bricks – Settings – Custom code” (see the screenshot below).

![](https://academy.bricksbuilder.io/wp-content/uploads/2020/04/bricks-builder-code-execution-1024x803.png)

Code Execution: Enabled for user role “Administrator”

Make sure to only enable code execution for users & user roles you trust 100%.

### How to add PHP & HTML code to your element

![](https://academy.bricksbuilder.io/wp-content/uploads/2020/04/bricks-builder-code-element-execution.png)

Code Element: Executing HTML & PHP code

Once you’ve enabled code execution you can start adding the “Code” element wherever you want to execute your code.

You’d usually execute PHP & HMTL code, as CSS & JS can be added much easier via the solutions outlined above.

Once you’ve added the Code element to your page, you can add your custom code to it (as shown in the screenshot ).

To run/execute the code, enable the “**Execute Code**” setting. Otherwise, the code just shows as a code snippet.

Click the “Sign code” icon at the top-right of the code editor (or CMD/CTRL + R) once you’ve finished editing your executable code.

### HTML Code Completion via Emmet

You can use abbreviations to generate your HTML structures much faster via a familiar CSS-based syntax.

**Abbreviation:** `#header` (+ TAB key)

**Generates:** `<div id="header"></div>`

**Abbreviation:** `h$[title=item$]{Header $}*3`

**Generates:**

```
<h1 title="item1">Header 1</h1>
<h2 title="item2">Header 2</h2>
<h3 title="item3">Header 3</h3>
```

[https://docs.emmet.io/cheat-sheet/](https://docs.emmet.io/cheat-sheet/)

---

*This documentation was extracted from the database for URLs containing 'bricks'*
