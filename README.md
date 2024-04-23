
# The Web Developer Bootcamp 2024 By Colt Steele

# My Notes
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


# HTML
## Intro
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
- Holding `option` and "clicking in multiple areas" creates multiple cursors if you want to add the same text to the same lines

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
- Superscript put text above line for reference call outs`<sup></sup>`   Sasquatch<sup><a href="somepage.html">[2]</a></sup>
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
    - Section is a generic place holder `<section>`
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
    - Table standard syntax 
        ```
        <table>
            
            <thead>     <!-- Head of table -->
            
                <tr>
                    <th>heading 1</th>      <!-- Headings of table -->
                    <th>heading 2</th>
                    <th>heading 3</th>
                </tr>
            
            </thead>

            
            <tbody>     <!-- Body of table -- >

                <tr>        <!-- Table row 1 -->
                    <td>test here</td>       <!-- Table text -->
                    <td>test here</td>
                    <td>test here</td>
                </tr>
                
                <tr>        <!-- Table row 2 -->
                    <td>test here</td>
                    <td>test here</td>
                    <td>test here</td>
                </tr>
            </tbody>

            <tfoot>     <!-- Footer of table -->
            </tfoot>

        </table>
        ```
    - For more complicated table formations use `<tr colspan="1">` and `<tr rowspan="2">`

## HTML Forms
- Form syntax
    ```
        <form action="/search/">
            <label for="cheese">Do you like cheese?</label>
            <input type="checkbox" name="cheese" id="cheese">
            <input type="text" placeholder="enter some text">
        </form>
    ```
- Inputs `<input type="text">` don't have a closing tag
    - Placeholder `<input type="text" placeholder="enter a username">`helps tell users what to enter inside input field
- Labels help identify ids submitted, like checkboxes, ids should be unique
    - They also make it so if you click on form text it will highlight the correct form field
    - Use `<label for="somename">` to reference "input" field id `<input type="text" id="username" name="username">`
    - The `name="username"` attribute is what gets sent during form submission 
        - `/search?username=tflande&password=yikes&color=%23d04949&num=4&time=13%3A29`
- Buttons in forms submit them `<button></button>`
    - Button `<button>Send</button>` and `<button type="submit">Send</button>` are the same inside a form
    - Button inside a form that wont submit `<button type="button">Send</button>`
    - Different way to do button as an input `<input type="button" value="Send it">` value is used to name the button, otherwise its call Submit by default
    - Buttons aren't required, user hits enter and form submits
- Check boxes
    - `checked` checks the box by default
        ```
            <form action="birds">
                <input type="checkbox" name="agree_tos" id="agree" checked>
                <label for="agree">I agree to everything!</label>
                <button>Send</button>
            </form>
        ```
- Radio buttons
    - Using the same `name` attribute makes a list of radio buttons in a group where only one can be selected, this is where the `id` attribute is important
        ```
        <!-- value attribute is needed -->
        <label for="xs">XS:</label>
        <input type="radio" name="size" id="xs" value="xs">
        <label for="s">S</label>
        <input type="radio" name="size" id="s" value="s">
        <label for="m">M</label>
        <input type="radio" name="size" id="m" value="m">
        ```
    - The value attribute is used to signal what radio button was selected once form has been submitted
        - `birds?agree_tos=on&size=s`
- Dropdown menus aka selects
    ```
    <label for="meal">Please select an entree</label>
    <select name="meal" id="meal">
        <option value="fish">Fish</option>
        <option value="veg">Vegetarian</option>
        <option value="steak" selected>Steak</option>       <!-- default menu item-->
    </select>
    ```
- Range sliders
    ```
    <label for="cheese">Amount of Cheese</label>
    <input type="range" id="cheese" name="cheese" min="1" max="100" step="2" value="75">     <!-- min max required>
    ```

# CSS
## Intro
- [MDN CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [CSS Online Coding, Book Store UI example](https://codepen.io/TurkAysenur/pen/JjGKKrP)
- [Color Picker](https://htmlcolorcodes.com/color-picker/)
- [Color Names](https://htmlcolorcodes.com/color-names/)
- [List on most common fonts found on Windows and/or Mac](https://www.cssfontstack.com/)

## CSS Selectors
- Selectors `p {}`, `a{}`, `h1 {}`, `h2, h3 {}` etc.
- id selector `#mybutton {}`: used to target html with `id="mybutton"`
    - Not commonly used 
- class selector `.cool_button {}`: used to select html with `class="cool_button"`
    - most used
- Descendant selectors
    - Direct selectors `h1 > p {}`: selects h1 one level down to paragraph
    - Adjacent selectors (combinator) `h1 + p {}`: Used to select paragraphs immediately followed by h1
- Attribute selector `input[type="text"] { width: 300px; color: yellow; }` used to select all attributes of said type "text"
    - Examples: 
        - Another option `section[class="post"] { color: red; }` is the same as saying `class="post"` in html and css reads `section.post { color:red; }`
        - `*` Select all links with work google in them using `*=` shown `a[href*=google] { color: pink; }`
        - `$` Select all link ending in .org `a[href$=".org"] { color: purple; }`
        - `~` Select all classes with word logo `a[class~="logo"] { padding: 2px; }`
- Pseudo classes :class
    - `:active`, `:hover`, `:checked`, `:first`, `:not`, `:nth-of-type`, and more etc
    - `:hover` Select all post class buttons: `.post button:hover { color: orange; }`
    - `nth-of-type(x)` Select every other post class `.post:nth-of-type(2n) { background-color: grey; }`
- Psuedo Elements
    - `::after`, `::before`, `::first-lettter`, `::first-line`, `::selection`, and more
    - `::first-letter` Make all h2 first letter bigger: `h2::first-letter { font-size: 50px; }`
    - `::first-line` Make all paragraph first lines purple `p::first-line { color: purple; }`
    - `::selection` Make all text selection orange: `::selection { color: orange; }`
### Which CSS selector takes precendence?
- Order matters! Last set wins
    - Last selector wins
    - Last css file specified in header wins
- CSS Specificity, which rules to apply when there is a conflict?
    - Order of precendence if used in css style sheet
        1. ID `#mybutton`
        2. Class `.classname`
        3. Elements `p, a`
    - Element vs Class - The more specific wins!
        - `button:hover { color: red; }` loses over `.post button:hover { color: orange; }`
    - Order precedence overall
        1. Don't use: Override inline styling of html `!important` is used in a css stylesheet `button { color:firebrick !important; }` override the below
        2. Don't use: Inline styling set inside html `<button style="color:red">Submit</button>`
        3. #ID
        4. .Class
        5. Elements
- [Specificity Calculator](https://specificity.keegan.st/)
## CSS Boxing
- Box borders require 3 parameters `border-style`, `border-color`, `border-width` to show up and `box-sizing` to remain within specified width constraints 
    ```
    #box1 {
        width: 100px;
        background-color: black;
        border-style: solid;
        border-color: black;
        border-width: 10px;
        box-sizing: border-box;
    }
    ```
    - Border short hand `border: medium dashed green`
        - Syntax: border: width | style | color
- Display Inline or Block
    - width and height are not ignored with regular block elements, but they are for normally inline elements
    - You can change from inline to block, but the above still applies
        - `display: inline;` to convert block level elements like h1, h2 to inline
        - `display: block;` to converrt normally inline like span to block
        - `display: none;` hides from browser view but html is still in page
- CSS sizes
    - px is pixels
    - em or m
        - 1em is 1x the size of parent size
        - 2em is 2x the size of parent size
        - 0.5 is half the size of the parent size
    - rems
        - scale better than em's
        - using pages default root size verus parent, 1rem will always be same as root or default
## Other CSS
- Resources
    - [Free Images unsplash](https://unsplash.com/)
    - [Google Fonts](https://fonts.google.com/)
    - [My Code](https://github.com/traceyflanders/Udemy - The Web Developer Bootcamp 2024/udemy_the_web_developer_bootcamp_2024/my_code/07_Other_Properties) 
- Alpha Color
    - Works only on background, background-color: rgba(255,255,255, 0.5) 4th channel 0 transparent to 1 not transparent
- Opacity
    - Works on text, opacity: 0.3; 0 to 1 being not transparent
- Position Property
    - position: `static` is default
    - position: `relative` keeps item in place relative its place in html location
        - top: 100px; push down 100px;
        - left: 100px; pushes to the right
    - position: `absoulute`
    - position: `fixed` good for navs
    - position: `sticky`
- Transistions
    - They are cool animations
    - Help with smooothing movement of items
- Transforms
    - Good for 3D animations movement
    - Rotate, resize, translate move positions, skew slants
    - [Transforms doc](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transforms/Using_CSS_transforms)
    - Use transforms instead of margins to move items
-CSS Button Hover
 - [box-shadow syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)
- Background 
    - https://developer.mozilla.org/en-US/docs/Web/CSS/background
    - https://developer.mozilla.org/en-US/docs/Web/CSS/background-size
- Fonts
    - Free fonts we can use [Google Fonts](https://fonts.google.com/)