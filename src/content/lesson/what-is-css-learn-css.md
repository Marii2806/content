---
title: "Learn CSS: What is CSS Meant for?"
subtitle: "As you may have noticed, HTML allows you to create only basic websites. Nobody wants to see a white website with some horrible text on it. So it's time to learn what CSS is all about! Learn CSS to make your website beautiful. Let's make it shine!"
cover_local: "../../assets/images/4cc6fa0b-2530-4052-aa7e-8dac03788ac3.png"
textColor: "white"
date: "2020-10-19T16:36:31+00:00"
tags: ["CSS"]
status: "published"

---

## Welcome to CSS!!

We are sure that after diving deep into HTML, everything looks kind of ugly, fixed, and rigid. We have to remember that HTML was created by CERN scientists, and they’re not usually the funniest kind of people (although they are the same exact scientists that [discovered The Higgs Boson](https://www.youtube.com/watch?v=0CugLD9HF94); and we do have to bow to our knees for that). However, HTML is still ugly, and it’s ugly because it was created for a different purpose than the one HTML meets today.

![what is css](https://github.com/breatheco-de/content/blob/master/src/assets/images/6891485c-2a5a-4722-a7dc-f108993c18ba.jpeg?raw=true)

But… The Internet is more beautiful than that. When the internet became popular, it stopped being only a privilege for scientists and the army, and evolved to become **part of our world!!**

Ironically, the same scientists at CERN who created HTML had to think about how to improve it. They were given the task of making it more beautiful. It was at this time that [Håkon Wium Lie](https://en.wikipedia.org/wiki/H%C3%A5kon_Wium_Lie) proposed the first version of CSS in 1994, which was later adapted to become CSS1.

## So, what is CSS, and why does it matter??

![what is css](https://github.com/breatheco-de/content/blob/master/src/assets/images/8c9fea86-c56c-486f-8b64-4322338076f7.jpeg?raw=true)

The main objective of his creation was to apply styles to HTML documents. The idea is to let you tell the browser how to display an HTML document: how to render its tags, in what color, margins, typography, icons, borders, etc. You can even redefine the original behaviors of the existing tags at your will. Ex:

```html
You could tell an <h1> to look just like an <h2> without the user realizing that, at first glance, they are different.
```

> :point_up:To understand the potential of CSS, [click here to see a live demo!](http://assets.breatheco.de/live-demos/css/bootstrap/)

Can you imagine the potential? You can make almost everything look different!

## How do I apply styles to HTML?

It's quite simple, you have to write your styles in a special syntax called "CSS" and save them on documents with the extension CSS.  Then, you apply the styles to the document using the `<link>` or the `<style>` tag.

Let’s review those 2 tags in more detail:

|**Name**   |**Tag**   |**Description**   |
|:----------|:-------------|:------------------|
|Link       |`<link>`          |The purpose is to link the page with CSS stylesheets.  To use it, you must specify three attributes within the tag: `rel="stylesheet" type="text/css"` and finally `href="with document route css"`<br>like so: `<link rel="stylesheet" type="text/css" href="theme.css"/>`   |
|Style   |`<style>`   |If we do not want or can’t import a CSS style sheet, we have the alternative to define styles in the HEAD of the HTML document.  We simply define the style tag and proceed to write the styles we want for the tags.<br>`<style>`<br>`h1 { color:red; }`<br>`p { color:blue; }`<br>`</style>` |

> :point_up: Just like it happens with HTML docs (ending with `.html`) CSS docs (style sheets) end with extension `.css`

## CSS Syntax

The CSS syntax is nothing similar to HTML syntax, it is its own specific programming language.  CSS does not use tags! To work with a website you have to shift your mindset several times because you will be working with several languages at the same time, and each one has its own syntax.

![learn css](https://github.com/breatheco-de/content/blob/master/src/assets/images/4a25cfd5-e8ab-4abb-b4f8-148d376b3f3d.gif?raw=true)

A CSS style sheet is a huge list of style definitions for each HTML element.  First, you must specify which element or group of elements you are going to style; this is called a SELECTOR.  Then you have to put a key `{` to indicate that you are going to start defining each attribute and its respective value, and you end that with another key `}`.  You should always finish each attribute definition with a semicolon `;`.

Watch the previous animation for a better understanding.

> :point_up:Spaces are ignored, but you need to use them to make your code easy to read.

The next example is a style sheet defining 3 different groups of styles (#id-selector, .class-selector, and tag-selector); and each of these groups has different rules applied like: color, font size, and background color.

You need to match HTML elements to groups of styles and use "selectors" to bind the HTML elements to the CSS groups of rules.

```css
#id-selector {
   color: red;
   font-size: 12px;
}
.class-selector {
   color: blue;
   background: green;
}
tag-selector 
{
   font-size: 15px;
}
```

## Wait… What is a "Selector"??

A selector is a way to refer to or identify one or more HTML elements. For example, if you want to change the color of your website to red, you must do as it follows:

```css
body {
    color: red;
}
```

You could also change the color of a single anchor `<a>`. To do that, you must define a `class` or an `id` attribute of the HTML tag defining that particular link `<a class="anchor1">`. Classes are a preferred use with CSS over IDs due to the fact that the former are reusable and the latter are more often used in conjunction with JavaScript. Once the tag has a class, then you can go to your style sheet and define the `color` rule as follows:

```css
.anchor1 {
   color: red;
}
```
The next tables show a list of all possible types of selectors available to use in CSS. Please take your time to review them carefully. Your understanding here is key to continue with CSS since you need to understand every possible style you can apply to an HTML doc:

### ID Selector

|**Selector**   |**Description**   |**Example**   |
|:--------------|:-----------------|:-------------|
|#element_id    |Allows the possibility to apply styles to a particular element   |`#element_id { color: red; }`   |

Let’s assign "first" as the ID of the first cell in the next table, and then with CSS we are going to specify that the ID "first" will have a yellow background:

<iframe width="100%" height="300" src="//jsfiddle.net/BreatheCode/1b78wna2/8/embedded/html,css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<div align="right"><small><a href="//jsfiddle.net/BreatheCode/1b78wna2/8/embedded/html,css,result/">Click here to open demo in a new window</a></small></div>

### Class selector

|**Selector**   |**Description**   |**Example**   |
|:-------------|:-----------------|:-------------|
|.classname   |There is an attribute in HTML called "class", which allows us to group different tags within one logical group.  With CSS we can use `.` (dot) as a selector of every element using the class name to select all html elements with that class attribute.   |`.classname { color: #BDBDBD; }`   |

In the next example we are applying an "odd" class to the cells of this table, and then with CSS we are assigning the yellow background to class .odd:

<iframe width="100%" height="300" src="//jsfiddle.net/BreatheCode/rdLkmx1t/11/embedded/html,css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<div align="right"><small><a href="//jsfiddle.net/BreatheCode/rdLkmx1t/11/embedded/html,css,result/">Click here to open demo in a new window</a></small></div>

### Tag selection

|**Selector**   |**Description**   |**Example**   |
|:--------------|:-----------------|:-------------|
|Element (tag) type   |This makes it possible to apply styles to links, titles, etc.  In the next example we shall change the text color of every link tag `<a>` on the page.   |`a { color: #BDBDBD; }`   |

Next, we are adding color (green) to the  background of each `td` (cells) of the table:

<iframe width="100%" height="300" src="//jsfiddle.net/BreatheCode/y89Lgwb0/11/embedded/html,css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<div align="right"><small><a href="//jsfiddle.net/BreatheCode/y89Lgwb0/11/embedded/html,css,result/">Click here to open demo in a new window</a></small></div>

### Multiselector

|**Selector**   |**Description**   |**Examples**  |
|:--------------|:-----------------|:-------------|
|selector1, selector2   |If you separate multiple selectors with a comma `,` you can assign multiple selectors at the same time to save text. In the following example we tell all the **h1** and **.odd** class elements, that we want their text to be red.   |`h1, .odd{ color: #BDBDBD; }`   |

### Pseudo selectors 

```css
a:link{color: green;}
a:visited{color: yellow;}
a:hover{color: blue;}
a:active{color: red;}
```

You can assign a different color to any link on the website, depending on its status:

+ `:link` default color, before clicking on it.
+ `:visited` after clicking the link.
+ `:hover` when the cursor is over the link.
+ `:active` when the cursor is clicking on the link.
  
  <iframe width="100%" height="300" src="//jsfiddle.net/BreatheCode/tLy9dvbr/2/embedded/html,css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<div align="right"><small><a href="//jsfiddle.net/BreatheCode/tLy9dvbr/2/embedded/html,css,result/">Click here to open demo in a new window</a></small></div>

### Advanced Selectors

With these 4 ways to select you are covering 99% of your needs; here what is important is to plan which will be on your Style sheet.

There are other specific and advanced selectors. You are probably going to use them when you start building something more challenging.

## Conflicts and correspondence

What happens if an element of the page is selected in two different selectors and has the green font color assigned to one definition and red in the other? In other words, if we have told the browser to find two different colors, what color will it end up getting?

![learn css](https://github.com/breatheco-de/content/blob/master/src/assets/images/08e78606-102f-4bc2-a066-7c26ae9400d5.png?raw=true)

You must have a very good understanding of the CSS hierarchy in order to understand how the elements **correspond, overwrite, and even null styles between them.**

The browser gives priority to more specific selectors like `#id` than the more general selectors like tags. In the following example, we changed the color of all the `<li>` (the items in the list) to blue, but then we changed the text of the second element to red. In this way we demonstrate that the ID selector will always prevail over selecting all the elements with the same tag.

<iframe width="100%" height="300" src="//jsfiddle.net/josemoracard/p6mbve3k/embedded/html,css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<div align="right"><small><a href="//jsfiddle.net/josemoracard/p6mbve3k/embedded/html,css,result/">Click here to open demo in a new window</a></small></div>

## Properties

We have already seen that a CSS style sheet is nothing more than a list that defines the properties that we want to assign to different elements of the page. Now we have to learn what properties we can assign to these elements.

There are hundreds – even thousands – of CSS properties, but depending on the type of element/label that we want to define, we must focus on specific properties.

#### Typography editing
|Property   |Description   |Values   |
|:----------|:-------------|:----------|
|[font-family](https://www.w3schools.com/cssref/pr_font_font-family.php)   |font type (font) |  name-font \| generic-family    |
|[font-size](https://www.w3schools.com/cssref/pr_font_font-size.php)   |size of the font   |absolute-size \| relative-size \| distance \| percentage   |
|[font-style](https://www.w3schools.com/cssref/pr_font_font-style.php)   |inclination (italics)   |normal \| italic \| oblique   |

#### Text editing

|Property   |Description   |Values   |
|:----------|:-------------|:-----------|
|[color](https://www.w3schools.com/cssref/pr_text_color.php)   |text color   |color   |
|[letter-spacing](https://www.w3schools.com/cssref/pr_text_letter-spacing.php)   |space between letters   |normal \| distance   |
|[line-height](https://www.w3schools.com/cssref/pr_dim_line-height.php)   |space between lines   |normal \| number \| distance \| percentage   |
|[text-align](https://www.w3schools.com/cssref/pr_text_text-align.php)   |text alignment   |center \| justify \| left \| right   |
|[text-decoration](https://www.w3schools.com/cssref/pr_text_text-decoration.php)   |text ornament   |none \| line-through \| overline \| underline   |
|[text-transform](https://www.w3schools.com/cssref/pr_text_text-transform.php)   |capital / small fonts   |none \| capitalize \| lowercase \| uppercase   |

#### List editing 

|Property   |Description   |Values   |
|:-----------|:-------------|:--------|
|[list-style](https://www.w3schools.com/cssref/pr_list-style.php)   |compound property (sum of every property combination)   |list-style-image \|\| list-style-position \|\| list-style-type   |
|[list-style-image](https://www.w3schools.com/cssref/pr_list-style-image.php)   |marker image   |none \| url   |
|[list-style-position](https://www.w3schools.com/cssref/pr_list-style-position.php)   |marker position   |inside \| outside  |
|[list-style-type](https://www.w3schools.com/cssref/pr_list-style-type.php)  |marker type   |none \| circle \| disc \| square \| decimal \| decimal-leading-zero \| lower-alpha \| upper-alpha \| lower-greek \| lower-latin \| upper-latin \| lower-roman \| upper-roman \| armenian \| georgian \| hebrew(-) \| cjk-ideographic(-) \| hiragana (-) \| katakana (-) \| hiragana-iroha(-) \| katakana-iroha(-)  |

#### Table editing

|Property  |Description   |Values   |
|:----------|:-------------|:-----------|
|[border-collapse](https://www.w3schools.com/cssref/pr_border-collapse.php)   |border mode   |collapse \| separate   |
|[border-spacing](https://www.w3schools.com/cssref/pr_border-spacing.php)   |space between cells   |distance \| distance   |
[caption-side](https://www.w3schools.com/cssref/pr_tab_caption-side.php)   |caption position   |top \| bottom    |
|[empty-cells](https://www.w3schools.com/cssref/pr_tab_empty-cells.php)   |empty box border   |	hide \| show   |
|[table-layout](https://www.w3schools.com/cssref/pr_tab_table-layout.php)   |	algorithm width of the table   |auto \| fixed   |

#### Background editing 

|Property   |Description   |Values   |
|:----------|:-------------|:----------|
|[background-color](https://www.w3schools.com/cssref/pr_background-color.php)   |background color   |transparent \| color   |
|[background-image](https://www.w3schools.com/cssref/pr_background-image.php)   |background image   |none \| url   |
|[background-position](https://www.w3schools.com/cssref/pr_background-position.php)   |background image position   | \[left \| center \| right \| distance \| percentage] [top \| center \| bottom \| distance \| percentage] |
|[background-repeat](https://www.w3schools.com/cssref/pr_background-repeat.php)  |background repetition   |no-repeat \| repeat \| repeat-x \| repeat-y \| space \| round   |
|[background-size](https://www.w3schools.com/cssref/css3_pr_background-size.php)   |background image size   |auto \| [distance \| percentage] \| contain \| cover   |


> 💡 Suggestion: 

 + [Follow this link to see a detailed list of CSS properties from W3Schools](https://www.w3schools.com/cssref)








 










