# UI-standards-and-Best-practices

A lot of coding best practices emphasize keeping code lean and well organized.The guidelines described here provide a brief introduction to CSS coding practice.

## 1. Use the Proper Document Structure
We must always use proper document structure, including the `<!DOCTYPE html>` doctype, and the `<html>`, `<head>`, and `<body>` elements. Doing so keeps our pages standards compliant and fully semantic, and helps guarantee they will be rendered as we wish.

## 2. Always avoid inline styling

Using inline styling show the HTML code messy. Updating each HTML events style through global CSS is hard. So you always need to avoid inline style. Below is the example related to this style:

```
Bad Code:
<div style="float:left">
    <img src="images/logo.gif" alt="" />
</div>
Good Code:
<div class="left">
    <img src="images/logo.gif" alt="" />
</div>
```

## 3.  Always use External CSS

Using an external stylesheet is very useful. Put all of your CSS in an external file, and have it included in your HTML. This is probably the best way to be sure to keep content and presentation separate.

### Advantages of using an external stylesheet:

    It helps to separate content from presentation.

    External stylesheets can be cached, allowing faster page loading times.

    A single stylesheet can be applied to every page of a site, allowing quick style changes to a single file.

    It makes organization much easier.

To use an external stylesheet, simply place the following code in between your head tags. Be sure to replace style.css with your CSS file.

```
<link rel="stylesheet" href="style.css" type="text/css" media="screen" />
```

## 4. Use Practical ID & Class Values

Creating ID and class values can be one of the more difficult parts of writing HTML. These values need to be practical, relating to the content itself, not the style of the content. 

```
Bad Code
<p class="red">Error! Please try again.</p>
              
Good Code
<p class="alert">Error! Please try again.</p>
```

 ## 5. Hyphens Instead of Underscores for CSS classes
 
 We should get into the habit of using hyphens instead while writing CSS classes and underscore for element IDs.

Example class:  .profile-image

Example ID:  #user_image

## 6. Organize your CSS-styles, using flags

“Divide your stylesheet into specific sections: i.e. Global Styles – (body, paragraphs, lists, etc), Header, Page Structure, Headings, Text Styles, Navigation, Forms, Comments, and Extras.

/* -----------------------------------*/

/* ---------->>> GLOBAL <<<-----------*/

/* -----------------------------------*/

Separate code into blocks. “This might be common sense to some of you but sometimes I look at CSS and it’s not broken down into “sections.” It’s easy to do and it makes working with code weeks, months, or years later much easier. You’ll have an easier time finding classes and elements that you need to change.

## 7. Shorthand CSS

One feature of CSS is the ability to use shorthand properties and values. Most properties and values have acceptable shorthand alternatives.
```
img {
    margin-top: 5px;
    margin-right: 10px;
    margin-bottom: 5px;
    margin-left: 10px;
}
button {
    padding: 0 0 0 20px;
}

Instead of above we can use shorthand CSS as follows:
img {
    margin: 5px 10px;
}  
button {
    padding-left: 20px;
}

Also:
.module {
    background: #DDDDDD;
    color: #FF6600;
}

Instead of above we can use shorthand CSS as follows:
.module {
    background:#ddd;
    color:#f60;
}
```

## 9. Minify CSS file size with CSS Compressors

It’s an excellent thought to minify the CSS file to reduce the file size. Through this, you can help browsers to accelerate the stacking of your CSS codes. So you can use a tool like CSS Compressor and Minifier to get this going.

You can minify your CSS here: https://csscompressor.net/

## 10. Cross-browser compatibility:

When you use an external stylesheet (where we can use browser engine prefix like -moz-, -webkit-, -o- and -ms-) for layout and valid markup (XHTML, HTML5), then your web pages work well on all browsers such as IE, Opera, Chrome, Mozilla, and Safari, etc..

Also following are the prefix description:
```
-moz- /* this is use for Firefox browser*/
-webkit- /*this is use for chrome and safari browsers*/
-o- /*this is use for opera browser*/
-ms- /*this is use for Internet Explorer (but not always it's depends on CSS3 browser support)*/
```
## 11. Organize the Stylesheet with a Top-down Structure
It always makes sense to lay your stylesheet out in a way that allows you to quickly find parts of your code. I recommend a top-down format that tackles styles as they appear in the source code. So, an example stylesheet might be ordered like this:

Generic classes (body, a, p, h1, etc.)
#header
#nav-menu
#main-content
**<editors-note>** Don't forget to comment each section! **</editors-note>**
```
/****** Generic content *********/

Resets and overrides.....

/****** main content *********/
 
styles goes here...
 
/****** footer *********/
 
styles go here...
```

## 12. Comment your CSS
Just like any other language, it's a great idea to comment your code in sections. To add a comment, simply add /* behind the comment, and */ to close it, like so:
```
/* Here's how you comment CSS */
```

## 13. Combine Elements
Elements in a stylesheet sometimes share properties. Instead of re-writing previous code, why not just combine them? For example, your h1, h2, and h3 elements might all share the same font and color:
```
h1, h2, h3 {font-family: tahoma, color: #333}
```
We could add unique characteristics to each of these header styles if we wanted (ie. h1 {size: 2.1em}) later in the stylesheet.

## 14. Use Multiple Classes
Sometimes it's beneficial to add multiple classes to an element. Let's say that you have a <div> "box" that you want to float right, and you've already got a class .right in your CSS that floats everything to the right. You can simply add an extra class in the declaration, like so:
    
```
<div class="box right"></div>
```
You can add as many classes as you'd like (space separated) to any declaration.
    
## 15. Make Use of Generic Classes
You'll find that there are certain styles that you're applying over and over. Instead of adding that particular style to each ID, you can create generic classes and add them to the IDs or other CSS classes (using #14).

For example, I find myself using float:right and float:left over an over in my designs. So I simply add the classes .left and .right to my stylesheet, and reference it in the elements.

```
.left {float:left}
.right {float:right}
 
<div id="coolbox" class="left">...</div>
```
This way you don't have to constantly add "float:left" to all the elements that need to be floated.

<editors-note> Please refer to editor's notes for #14. </editors-note>

## 16. Use Text-transform
Text-transform is a highly-useful CSS property that allows you to "standardize" how text is formatted on your site. For example, say you're wanting to create some headers that only have lowercase letters. Just add the text-transform property to the header style like so:

```
text-transform: lowercase;
```
## 17. Ems vs. Pixels
There's always been a strong debate as to whether it's better to use pixels (px) or ems (em) when defining font sizes. Pixels are a more static way to define font sizes, and ems are more scalable with different browser sizes and mobile devices. With the advent of many different types of web browsing (laptop, mobile, etc.), ems are increasingly becoming the default for font size measurements as they allow the greatest form of flexibility.

## 18. Validate Your CSS and XHTML
Validating your CSS and XHTML does more than give a sense of pride: it helps you quickly spot errors in your code. If you're working on a design and for some reason things just aren't looking right, try running the markup and CSS validator and see what errors pop up. 


## 19. Add Margins and Padding to All
Different browsers render elements differently. IE renders certain elements differently than Firefox. IE 6 renders elements differently than IE 7 and IE 8. While the browsers are starting to adhere more closely to W3C standards, they're still not perfect (*cough IE cough*).

One of the main differences between versions of browsers is how padding and margins are rendered. If you're not already using a reset, you might want to define the margin and padding for all elements on the page, to be on the safe side. You can do this quickly with a global reset, like so:

```
* {margin:0;padding:0;}
```
## 20. Use a Reset
Most CSS frameworks have a reset built-in, but if you’re not going to use one then at least consider using a reset. Resets essentially eliminate browser inconsistencies such as heights, font sizes, margins, headings, etc. The reset allows your layout look consistent in all browsers.

## 21. Use multiple stylesheets
Depending on the complexity of the design and the size of the site, it’s sometimes easier to make smaller, multiple stylesheets instead of one giant stylesheet. Aside from it being easier for the designer to manage, multiple stylesheets allow you to leave out CSS on certain pages that don’t need them.

For example, I might have a polling program that would have a unique set of styles. Instead of including the poll styles to the main stylesheet, I could just create a poll.css and the stylesheet only to the pages that show the poll.

However, be sure to consider the number of HTTP requests that are being made. Many designers prefer to develop with multiple stylesheets, and then combine them into one file. This reduces the number of HTTP requests to one. Also, the entire file will be cached on the user’s computer.

## 22. Keep a Color Reference
Include a reference at the top of your CSS file. 
```
/* reference css
background: #FFCCCC
normal text: #FFF46D
font-size: 12em
*/

master.css
@import url("reference.css");
h1 {
background: background
font-size: font-size
```
## 23. Use a master stylesheet
Let me quote this piece of advice from its original source:

“One of the most common mistakes I see beginners and intermediates fall victim to when it comes to CSS is not removing the default browser styling. This leads to inconsistencies in the appearance of your design across browsers, and ultimately leaves a lot of designers blaming the browser. It is a misplaced blame, of course. Before you do anything else when coding a website, you should reset the styling.” [Master Stylesheet: The Most Useful CSS Technique], [Ryan Parr]

```
master.css
@import url("reset.css");
@import url("global.css");
@import url("flash.css");
@import url("structure.css");
<style type="text/css" media="Screen"> /**/@import url("css/master.css");/**/ </style>
```
Conclusion:

We have listed out best practices which every front-end and back-end developer follows. Also if the beginner level developer follows these guidelines.

This approach is quite practical for both front-end and back-end developers.
