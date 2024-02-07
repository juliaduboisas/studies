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

