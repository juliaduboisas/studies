# How it works

## Page requests and URLs

- it's common that networks use a LAN or a WAN
    - LAN -> local area network
    - WAN -> wide area network
- every URL (Uniform Resource Locator) has three parts:
    - protocol -> how to connect
    - domain -> server
    - (optional) document -> specific file needed
        - most pages are made up of multiple files
- protocols
    - HTTP (hypertext transfer protocol)
    - HTTPS (secure hypertext transfer protocol)
    - FTP (file transfer protocol)
- domanin names
    - identifies the entity you want to connect to
    - each has a different top-level domain (.com, .edu etc)
        - determined by the Internet Corporation for Assigned Names and Numbers (ICAAN)
- IP Adresses
    - Internet Protocol Version 6 (IPv6) is the communication protocol that idetifies computers on networks
    - every computer has a unique IP address xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx where x can have 16 different values
- document
    - URLs can specify a document
    - if no document is specified, it will return the default document (usually index.html)

- the request
    - once the IP address is determined, the browser creates an HTTP request
    - lots of hidden info in this request (header, cookied, form data etc)
- the response
    - the server returns files, not "web pages", and it is up to the browser to decide what to do with those files
    - if the servevr can't fulfill the request it will sent back files with error codes

# Tools and tips

## Browsers and accessibility

- http://www.html5accessibility.com/ keeps a review of the accessibility of browsers
- browsers should have
    - keyboard functionality
    - support HTML5 tags
    - support features for assistive technology
- browsers can vary in how well they adhere to HTML5 standards
- different versions of browsers need to be considered as well
- test in a variety!!

## How to use an editor to create an HTML file

- creating and editing your files
    1. decide how you will organize your files
    2. decide on a naming convention
    3. decide on an editor
- getting started
    1. open your editor
    2. select "Save" or "Save As" and name your file, may need to create a folder first
    3. add doctype, head, and body tags
    4. save file
    5. open in browser
- troubleshooting
    - file opens in an editor instead of a browser -> right click and select "Open With"
    - browser shows tags -> check that the file extension is .html
    - changed code but page still looks the same -> refresh browser, verify file name
    - "weird" characters -> try typing code in by hand, not copy-and-paste

# The Document Object Model (DOM)

- Basis of HTML5 is "New features should be based on HTML, CSS, the DOM, and JavaScript [...]"
- DOM provides common tree-like structures that all pages should follow
- Computer Scientists love trees because you can test them
- HTML is built on the DOM
    - two parts: head and body
    - head: information the user isn't going to see (metadata)
    - body: all HMTL5 tags (displayable content)
    - at the root is the html tag (DOCTYPE)

- Doctype
    - !DOCTYPE html

- head
    - additional info used by the browser
        - metadada (lang, title)
        - supporting files (JS, styling, add-ons)
    - other than the title, metadata is not displayed

- body
    - bulk of the page
    - important to write well-formatted (aka tree-like) code
        - every tag NEEDS an end
    - most of the content is displayed by the browser, but there may be some metadata too

- validate the code
    - https://validator.w3.org
    - can validate by URL, by file or direct input
    - don't worry about warnings
    - sometimes one error can cause a lot of other errors

- review
    - well-formatted pages use the DOM structure
        - use beginning and end tags
        - close inner tags before outer ones
        - use valid attributes
    - browsers will "fix" bad code, but not always well -> use a validator to check your code

# HMTL Tags

## Syntax tags

- every tag has a beginning <start> and an end </end>
    - some tags are self-closing <tag>
- some tags have attributes (src, href etc)
    - display -> one of the most important attributes of an element
        - block (can take width and height) -> newline is inserted before and after, eg it "takes up" the whole width
        - inline (cannot take width and height) -> only uses as much space as needed to contain the element
- common tags
    - headings (block)
        - h1, h2, h3 etc
        - have syntax and semantics
            - things in h1 has much more importance than h2 and so it goes, affects screen readers
    - paragraphs (block)
        - p ... /p
        - should only contain inline elements
    - div (block)
        - div ... /div
        - generic section that is larger than a paragraph
    - ordered lists (ol, li)
    - unordered lists (ul, li)
    - line breaks (br)
- attributes
    - attributes provide additional information about an element
    - always specified in the start tag
    - attributes come in name/value pairs
    - some types
        - class -> applies special properties to groups of elements
        - id -> specifies a unique id to one element on the page
        - style -> specifies a certain visual style (avoid!!)
        - accesskey -> shortcur key to activate an element
        - tabindex -> order elements will come into focus using the key
- images
    - inline: img src="name.jpg" alt="smallDescription" title="titleOnHover" class"extraFormatting"
    - images rarely work the first time
        - size and carefully name your picture before you use it
- special entities can be used for certain characters(research when needed)

- resources:
    - WPKube cheatsheet: https://www.wpkube.com/html5-cheat-sheet/
    - https://htmlcheatsheet.com/
    - Webaim cheatsheet: https://webaim.org/resources/htmlcheatsheet/


## Semantic tags

- how to design
    - the most important step in web design is the design itself
    - you need a clear picture of what you want to create before you can begin coding
    - semantic tags help guide users to information in your page
- using semantic tags
    - in the beginning there was div
    - div was a way to group related content together
    - divs always always had special classes/ids associated with them
- header
    - a group of introductory or navigational aids: title, navigation links etc
    - not to be confused with head or different headings
- nav
    - section of the page that links to other pages or parts within the page
    - often found in the header tag
- footer
    - contains info such as copyright data, related documents and links to social media
    - tipically at the bottom of the page, but not required
- figure
    - more semantics than img
    - can include
        - caption
        - multiple multimedia resources

- resources: https://www.w3schools.com/html/html5_semantic_elements.asp