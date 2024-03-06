
# The Web Developer Bootcamp 2024 By Colt Steele

- [Course Link on Udemy.com: The Web Developer Bootcamp 2024 By Colt Steele](https://www.udemy.com/share/101W9C3@tnDbvQIOfdQtnl4Ik-tzoOyk3E8v5IoZV1TSct5vvUCZb89h8-mBdqoGD9aHCYHM/)


# Course Documentation
- Project Local Folder: ```/Users/tflande/My Drive/Projects/Udemy - The Web Developer Bootcamp 2024/udemy_the_web_developer_bootcamp_2024```
- [GitHub Markdown Syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Trello Board for Course *(Colored coded by difficulty)*](https://trello.com/b/0PVRE1XQ/web-developer-bootcamp)
- [Mozilla Documentation](https://developer.mozilla.org/en-US/docs/Web) 
    - [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
    - [Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
    - [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
    - [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- Github Code Course Repository
  - [TheWebDeveloperBootcampSolutions](https://github.com/Colt/TheWebDeveloperBootcampSolutions)

# Software Install
- Install [Visual Studio Code](https://code.visualstudio.com/Download) from Microsoft *(Billy Gates)*
- VS Studio Colts' Recommended Extensions https://www.youtube.com/watch?v=rH1RTwaAeGc&t=1s
  - Emmet installed by default
    - `<li*5`
  - Material Theme: Paleknight high constrast
  - Live Server


# Lessons
## HTML Intro
- Sample text https://en.wikipedia.org/wiki/Chicken
    ```
    <!DOCTYPE html>
    <html>
        <head>
            <title>My First Page</title>
        </head>
        <body>
            <!-- Content goes here -->
        </body>
    </html>
    ```


## VS Code Shortcuts
- VS User Settings: `cmd + ,`
- HTML boilerplate: `!` tab key
    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        
    </body>
    </html>
    ```
- Command Palette: `cmd + shift + p`
- Format code: `option + shift + f`
    - You can also auto enable auto formatting by searching VS *user settings* for "format", and also "format html" to turn it on for just html.
- Duplicate lines `shift + option + down arrow` or  `shift + option + up arrow`
- Comment in html: `cmd + /`

## HTML elements
- Lists
    - Unordered List`<ul></ul>`
    - Ordered List `<ol></ol>`
    - List item `<li></li>`
- Images have no closing bracket `<img src="filename.jpg" alt="alternate text if picture isn't found or a screenreader is used">`
- Block content to format with CSS `<div></div>`
- Inline content to format with CSS `<span>some text</span>`
    - Unline block its used to format things inline on same line versus creating a block lik `<div>`
- Line break, no ending /br `<br>`
- A line, not ending /hr`<hr>`
- Superscript put text above line for reference call outs`<sup></sup>`   Saquatch<sup><a href="somepage.html">[2]</a></sup>
- Subscript put text below line scientific formulas `<sub></sub>`   H<sup><a href="somepage.html">2</a></sup>O or H<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>
  - Together Superscipt and Subscript can make fractions `<sup>1</sup>/<sub>2</sub> + <sup>1</sup>/<sub>2</sub> = 1`   <sup>1</sup>/<sub>2</sub> + <sup>1</sup>/<sub>2</sub> = 1   
- HTML Entities are like copyright symbols, degrees symbols
    - Start with`&` and end with `;`
    - Examples:
        - less than &lt; `&lt;`
        - greater than &gt; `&gt;`
        - Ampersand &amp;`&amp;`
        - Heart &hearts; `&hearts;`
        - Spade &spades; `&spades;`

## Semantic Markup 
Newer way to group content versus just using divs, helps crawlers to identify what are "navs", "main" page content, "footers" etc. Categories your page content for better SEO, accessible.
- Bad example: medium.com
- Good example: stripe.com
    - Navigation `<nav>`
    - Main page content not navigation or search`<main>`
    - Section is a generic place holder `<section>` can you in place of nav
    - Article for reusable code like a widget, has heading `<article>`
    - Aside is a side note `<aside>`
    - Header `<header>` used above things in page, its not the head
    - Footer of page, you can have more than one per page `<footer>`
    - Time `<time datetime="2024-03-05">July 7</time>`  <time datetime="2024-03-05">July 7</time>
    - Figure is a pic with a caption or could use a div
        - ```
            <figure>
                <img src ="somefile" alt="wolf">
                <figcaption>A wolf in the wild</figcaption>
            </figure>
            ``` 
    - And many more `<data>`

## Screen Reader Demo of Stripe.com
- On Mac `cmd + F5`
    
## Emmet Syntax Demo
- Make your html coding fast ffs! Emmet is built into VS Code
- [Cheat sheet](https://docs.emmet.io/cheat-sheet/)
- Create new page
    - `!` tab key
        ```
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>
        </head>
        <body>
            
        </body>
        </html>
        ```
    - Create "nested" html `main>section>h1` tab key
        ```
        <main>
            <section>
                <h1></h1>
            </section>
        </main>
        ```
    - Create "sibling" html `h1+h2+h3` tab key
        ```
        <h1></h1>
        <h2></h2>
        <h3></h3>
        ```
    - Create 5 of the same li `<li*5`
        ```
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        ```
    - Create nested and multiples `nav>ul>li*3>a`
        ```
        <nav>
            <ul>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
                <li><a href=""></a></li>
            </ul>
        </nav>
        ```
    - Use  `$` and [href=] to auto enumerate with `nav>ul>li*3>a[href=www.$.net]`
        ```
        <nav>
            <ul>
                <li><a href="www.1.net"></a></li>
                <li><a href="www.2.net"></a></li>
                <li><a href="www.3.net"></a></li>
            </ul>
        </nav>
        ```
    - Use `{}` for adding in text `nav>ul>li*3>a[href=www.$.net]{Click me}`
        ```
        <nav>
            <ul>
                <li><a href="www.1.net">Click me</a></li>
                <li><a href="www.2.net">Click me</a></li>
                <li><a href="www.3.net">Click me</a></li>
            </ul>
        </nav>
        ```

## HTML Tables
- Bad Examples of using tables in the 1900's
    - [Wikipedia](https://en.wikipedia.org/wiki/List_of_largest_cities#List) 
    - [Bob Dole](http://www.dolekemp96.org/main.htm)
- [Bird Species](https://en.wikipedia.org/wiki/Largest_organisms#Heaviest_living_bird_species)
    - 