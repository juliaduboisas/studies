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