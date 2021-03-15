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











