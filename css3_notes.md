<h1 align=center>----- Basics -----</h1>

## Link Pseudo-Classes
Commonly used pseudo-classes for styling hyperlinks:

1. :link - selects unvisited links
2. :visited - selects visited links
3. :hover - mouse is hovering over a link
4. :active - the state when clicking on a link; this is brief
5. :focus - when a user focuses on a link - seen when tabbing to a link or after clicking on a link

The suggested link order is:

    a -> a:link -> a:visited -> a:hover -> a:focus -> a:active

<h1 align=center>----- Best Practicees -----</h1>

#### Floats First
Place floated elements first in the document order. They require something to wrap around, otherwise they may create a step down effect.

#### Always set a ```type``` on ```<button>```>
The default value is ```submit```, which means any button in a form may submit the form. If the button does not submit the form, use ```type="button"```.

    <button type="submit">Submit Form</button>
    <button type="button">Cancel</button>
    
