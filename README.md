# UI-standards-and-Best-practices

A lot of coding best practices emphasize keeping code lean and well organized.The guidelines described here provide a brief introduction to CSS coding practice.

#Use the Proper Document Structure
We must always be sure to the use proper document structure, including the <!DOCTYPE html> doctype, and the <html>, <head>, and <body> elements. Doing so keeps our pages standards compliant and fully semantic, and helps guarantee they will be rendered as we wish.

## 1. Always avoid inline styling

Using inline styling show the HTML code messy. Updating each HTML events style through global CSS is hard. So you always need to avoid inline style. Below is the example related to this style:

Bad Code:
<div style="float:left">
    <img src="images/logo.gif" alt="" />
</div>
Good Code:
<div class="left">
    <img src="images/logo.gif" alt="" />
</div>

## 2.  Always use External CSS

Using an external stylesheet is very useful. Put all of your CSS in an external file, and have it included in your HTML. This is probably the best way to be sure to keep content and presentation separate.

Advantages of using an external stylesheet:

It helps to separate content from presentation.
External stylesheets can be cached, allowing faster page loading times.
A single stylesheet can be applied to every page of a site, allowing quick style changes to a single file.
It makes organization much easier.

To use an external stylesheet, simply place the following code in between your head tags. Be sure to replace style.css with your CSS file.

<link rel="stylesheet" href="style.css" type="text/css" media="screen" />

# Use Practical ID & Class Values

Creating ID and class values can be one of the more difficult parts of writing HTML. These values need to be practical, relating to the content itself, not the style of the content. 

Bad Code
<p class="red">Error! Please try again.</p>

              
Good Code
<p class="alert">Error! Please try again.</p>

 # Hyphens Instead of Underscores for CSS classes
 
 Get into the habit of using hyphens instead while writing CSS classes and underscore for element IDs.

Example class:  .profile-image

Example ID:  #user_image
