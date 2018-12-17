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
Conclusion:

We have listed out best practices which every front-end and back-end developer follows. Also if the beginner level developer follows these guidelines, they will not miss a single point while they are writing the CSS.

This approach is quite practical for both front-end and back-end developers.
