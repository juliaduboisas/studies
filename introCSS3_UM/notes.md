# CSS: Cascading Style Sheets

- browser default styling: usually really plain
- cascading style sheet
    - CSS defined generic rules that can apply to multiple elements
- adding style
    - as styling tags were phased out of HTML, styling was done with the style attribute
        - this violates the separation of content and style
- CSS defined generic rules that can apply to multiple elements
    - with the selector you choose what you want to style
    - inside it you choose what you want to change
        
        selector {
            property:value;
        }

    - brackets and semicolons are very important
        - this is where a good editor can make a BIG difference
    - comments are in the same way as C
    - you can have as many property/value pairs as you want
- internal style sheet
    <code>
        <head>
            <meta charset="UTF-8">
            <title>Title here</title>
            <style>
                h1{
                    color:blue;
                }
            </style>
        </head>
    </code>
    - styles are applied to all elements in that file
- external style sheet
    - you can put rules in an external file (don't use the style tag!!)
    - a link to the style sheet is put in the head section
        <code> 
            <link rel="stylesheet" href="style.css">
        </code>
    - styles are applied to all elements in all files that links to the style sheets

# The "Cascading" of CSS

- order of precedence (lowest to biggest)
    - Browser default
    - External style
    - Internal style
    - Inline style
- if one selector is defined in two different
    - the most recent rule has preference (with insider code or external styles)
- if you use the !important tag, it overrides the rest

# Colors

- color conventions
    - color names work, but should be avoided (use hex or RGB or RGBa)
- accessibility
    - appropriate use of color is critical to web accessibility
    - many more people are visually impaired or color blind than are legally blind
    - color contrast tools
        - http://wave.webaim.org/
        - http://webaim.org/resources/contrastchecker/
    - don't use color alone to convey meaning

- review
    - use web safe colors and use an accepted convention
    - test your site using a contrast checker
    - avoid using color to convey meaning

# Styling your text

- options
    - font (family, style, variant, size)
    - color and background
    - alignment
    - line-height
- font-family
    - font families are styles of text
    - not all font-families are supported by all the operating systems, so you can provide alternatives
    - some fonts are not as user-friendly, use sans-serif when possible
    - custom fonts -> to expand beyond "web-safe"" fonts use @font-face
    <code>
        @font-face{
            font-family: specialFont;
            src: url('font.ttf');
        }
    </code>
- font-style
    - normal
    - italic
    - oblique
- font-variant
    - normal
    - small-caps
- font-size
    - options
        - xx-small, x-small, small, smaller
        - medium
        - large, larger, x-large, xx-large
        - use pixel
        - use %
- color and background-color
    - the color attribute is the color of the foreground
    - the background-color is the color of the background
- text-align
    - left
    - right
    - center
    - justify
- line-height
    - doesn't affect the font, adjusts the space between the lines of text

- review
    - the number of options for styling text can seem overwhelming
    - practive on toy problems
    - design larger projects on papar first

# Display and visibility

- display is key to layout
    - every element is a box
    - display affects the layout of neighbouring elements
- common values
    - inline: sit next to other elements
        - takes up "just enough" width and height
    - block: forces line break
        - default: take up all horizontal width and "just enough" height
        - rules can set height and width
    - inline-block: same as inline, but accepts height and width
    - none: removed from page
        - still in DOM, but not visual
- complementary properties
    - float
        - reposition elements to the right or left
        - elements are aware of one another and will not overlap
        - values: left, right
    - clear
        - used to keep floating elements away
        - values: left, right, both
- element overflow
    - visible: can cause text to show up "on top" of other text
    - hidden: hides anything that goes beyond bounding box
        - this can cause problems since if the user increases font size, they may not be able to see content
    - scroll: gives horizontal and verticle scrollbars
    - auto: adds scrollbars as needed
- other display values
    - table
    - grid
    - flexbox
- visibility
    - specifies whether or not the element is visible
    - options
        - visible
        - hidden
        - collapse (only for table elements)
    - unlike display:none a hidden element is still part of the DOM  and still takes up space

- review
    - display is just one tool for positioning our elements on the page
    - early design will make the coding easier
    - utilize tools to see the different options

## Display: Grid
- steps
    1. set display to grid
    2. set grid-template-columns to number and size of columns
    3. set justify-content

## Display: Flex
- you can use if you want to let the browser resize your elements based on the screen size
- you need to define a *parent* element and give it *children* elements
- how to
    - parent element
        1. set display to fle
        2. set flex-wrap to wrap or nowrap
        3. set flex-direction to row or column
        4. set the justify-items and/or align content
    - children elements

## Styling links and lists
- links are what make up a website, are super important
- additional property: text-decoration
- many designers want links to look like buttons, instead just use an actual button
- different linkk states
    - a:link -> normal, unvisited
    - a:visited -> already visited
    - a:hover -> what happens when hovering, doesn't exist in mobile
    - a:focus -> tapping
    - a:active -> when clicking
- some list properties
    - list-style-type
    - list-style-image
    - list-style-position
    - list-style

# Navigation
- navigation should be styled differently from the rest of the page
- to choose only the navigation links use "nav a" as the tag
- choose a different background color
- use list formatting to format the navigation

# Browser Capabilities
- handling stylistic differences
    - "easiest" way to eliminate browser differences is to use a default style sheet
        - reset all values for your values for the page
- handling unsupported properties
    - browser prefices provide a quick fix to unsupported CSS3 properties
        - -webkit-
        - -moz-
        - -ms-
        - -o-
    - some common unsupported properties
        - column-count
        - border radius
        - gradient
        - www.caniuse.com
- automated ways to include prefixes
    - editor add-ons
    - outside programs to dynamically add appropriate prefix based on browser
