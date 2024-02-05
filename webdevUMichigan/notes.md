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