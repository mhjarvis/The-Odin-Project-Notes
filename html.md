<h1 align=center>----- Links -----</h1>

1. HTML Intro: https://learn.shayhowe.com/html-css/
2. HTML Code Validation: https://validator.w3.org/
3. CSS Code Validation: https://jigsaw.w3.org/css-validator/

<h1 align=center>----- Basics -----</h1>

## Building Basics

    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <title>Title to display in Browser tab</title>
            <link rel="stylesheet" href="main.css">
        </head>
        <body>
            <h1>Heading</h1>
        </body>
    </html>

#### CSS Resets
Resets should be at the top of a stylesheet, since rendering happens from top to bottom. Eric Meyer reset: https://meyerweb.com/eric/tools/css/reset/

    /* http://meyerweb.com/eric/tools/css/reset/ 
    v2.0 | 20110126
    License: none (public domain)
    */

    html, body, div, span, applet, object, iframe,
    h1, h2, h3, h4, h5, h6, p, blockquote, pre,
    a, abbr, acronym, address, big, cite, code,
    del, dfn, em, img, ins, kbd, q, s, samp,
    small, strike, strong, sub, sup, tt, var,
    b, u, i, center,
    dl, dt, dd, ol, ul, li,
    fieldset, form, label, legend,
    table, caption, tbody, tfoot, thead, tr, th, td,
    article, aside, canvas, details, embed, 
    figure, figcaption, footer, header, hgroup, 
    menu, nav, output, ruby, section, summary,
    time, mark, audio, video {
    	margin: 0;
    	padding: 0;
    	border: 0;
    	font-size: 100%;
    	font: inherit;
    	vertical-align: baseline;
    }
    /* HTML5 display-role reset for older browsers */
    article, aside, details, figcaption, figure, 
    footer, header, hgroup, menu, nav, section {
    	display: block;
    }
    body {
    	line-height: 1;
    }
    ol, ul {
    	list-style: none;
    }
    blockquote, q {
    	quotes: none;
    }
    blockquote:before, blockquote:after,
    q:before, q:after {
    	content: '';
    	content: none;
    }
    table {
    	border-collapse: collapse;
    	border-spacing: 0;
    }

<h1 align=center>----- Getting to Know HTML -----</h1>

## Divisions and Spans

Divisions (```<div>```) and spans (```<span>```) are elements that act as containers primarily for styling purposes. a ```<div>``` is a block-level element and is mainly used to identify large groupings of content. A ```<span>``` is an inline-level element used to identify smaller groupings of text within a blcok-level element.

#### Block vs Inline Elements
Block-level elements begin on a new line, stacking on top of another, and occypying any available width. They must be nested inside one another and may wrap inline-level elements. 

Inline-level elements do not begin on a new line. They line up one after another and only maintain the width of their content. They can be nested inside another but cannot wrap block-level elements.

## Using Text-based Elements
#### Headings
Six different rankings...```<h1>``` through ```<h6>```. These help break up webpages for users and are used by search engines to index and determine the content on a page. Use in order.

#### Paragraphs
These are defined with the ```<p>``` block-level element.

#### Bold Text with Strong
Use the ```<strong>``` or ```<b>``` in-line element. The ```<strong>``` element is for content that is of greater importance, while ```<b>``` is used to draw attention to text without indivating that it's more important. If you want to bold text for decoration, instead use ```font-weight```.

    <strong>                        //use for content that is of greater importance
    <b>                             //use to draw attention to text without indicating that it is more important
    <font-weight>                   //use for decorative bolding
    
Example:

    <p><strong>Caution</strong> Danger Ahead!</p>           //proper use of <strong>
    <p>This recipe needs <b>bacon</b> ...</p>               //proper use of <b>
    
#### Italicize Text with Emphasis
The ```<em>``` element is used semantically to place a stressed emphasis on text. The ```<i>``` element is used to convey text in an alternative voice or tone. 

    <p>I <em>love</em> Chicago!</p>
    <p>The name <i>Tom</i> means something.</p>
    
## Building Structure
#### Header
The ```<header>``` element is used to identify the top of a page, article, section, or other segment of a page. May include heading, intro text, navigation.

    <header>

#### Navigation
The ```<nav>``` element identify navigational links on a page. Use for global navigation, table of contents, previous/next links, and other noteworthy groups of navigational links.

    <nav>

#### Article
The ```<article``` element is used to identify a section of independent, self-contained content that may be independently distributed or reused. Examples include blog posts, newspaper articles, user-submitted content, etc. The content within an article tag might be replicated elsewhere without confusion. 

    <article>

#### Section
The ```<section>``` element is used to identify thematic grouping of content (may include a heading). Commonly used to break up and provide hierarchy to a page.

    <section>
    
#### Deciding between ```<article>```, ```<section>```, or ```<div>``` Elements
Use ```<div>``` if the content is used only for styling purposes. The other are best to provide structure to a page.

#### Aside
The ```<aside``` element holds content such as sidebars, inserts, or brief explanations. Remember that this is a block-level element.

    <aside>
#### Footer
The ```<footer>``` element the closing or end of a page, article, section, or other segment of a page. 

    <footer>
    
## Creating Hyperlinks
Hyperlinks are established using the anchor (inline) element ```<a>```. To create a link from one page to another use the hyperlink reference ```href```. ```href``` identifies the destination of the link. Despite being a inline element, the anchor element is able to wrap block level elements in order to make entire sections clickable as links.

    <a href="somelink....com">Click here!</a>
    
#### Relative & Absolute Paths
Links pointing to a page on the same website will have a relative path. Links to other websites use a absolute path. 

    <a href="about.html">About</a>                  //relative path
    <a href="duckduckgo.com">Duck</a>               //absolute path
    
#### Linking to an Email Address
To create an email link, the href attribute value needs to start with ```mailto:``` followed by the email address. Subject, body text, and other information for the email can also be populated. The first parameter following the email address must begin with a question mark ```?```. This binds it to the hyperlink path. Multiple words requireing spaces must be encoded ```%20```. Adding body text works using the ```body=``` parameter and using the ampersand ```&``` to seperate the two. 

    <a href="mailto:markus@gmail.com?subject=Question%20for%20you">Email me</a>

#### Open Links in a New Window
To open links in a new window, use the ```target``` attribute with a value of ```_blank```.

    <a href="http://duckduckgo.com" target="_blank">Click here!</a>                 //opens in new window
    
#### Linking to Parts of the Same Page
We can link to different parts of the same page by first creating an ```id``` element. We then use the value of that id attribute in the anchor element's href attribute. 

    <body id="top">
    ...
        <a href="top">Back to top</a>
    ...
    </body>

<h1 align=center>----- Getting to Know CSS -----</h1>
<h1 align=center>----- Opening the Box Model -----</h1>
<h1 align=center>----- Positioning Content -----</h1>
<h1 align=center>----- Working with Typography -----</h1>
<h1 align=center>----- Setting Backgrounds & Gradients -----</h1>
<h1 align=center>----- Creating Lists -----</h1>
<h1 align=center>----- Adding Media -----</h1>
<h1 align=center>----- Building Forms -----</h1>
<h1 align=center>----- Organizing Data with Tables -----</h1>
<h1 align=center>----- Writing Your Best Code -----</h1>
































