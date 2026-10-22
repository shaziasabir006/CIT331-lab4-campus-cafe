# HTTP observations (Lab 4, Task 1)

Fill these with YOUR measurements from Chrome DevTools using Live Server (http://127.0.0.1:5500), not file://.

| Question | My answer |
|---|---|
| Request method for index.html | TO MEASURE |
| Status code with Disable cache ticked | TO MEASURE |
| Status code on a normal reload | TO MEASURE |
| Status code for /nothing-here.html | TO MEASURE |
| Value of the Content-Type response header | TO MEASURE |
| Remote Address (IP and port) | TO MEASURE |
| Protocol in the address bar (http or https) | TO MEASURE |

## Why is this address http and not https?
The local development server uses HTTP for testing on my own computer. HTTPS encrypts traffic across a network and is used on the published GitHub Pages website.

## Bug log
The supplied debug page has been prepared in a corrected state. For the lab's before/after requirement, recreate the instructor's original ten-fault version, commit it on task6-bug-hunt, then document the ten fixes here and commit the corrected version.

## Bug log (Lab 4, Task 6)

| # | What was wrong | Tool | My fix |
|---|---|---|---|
| 1 | HTML had no lang attribute | Lighthouse | Added lang="en" |
| 2 | Stylesheet pointed to style.css instead of bugs.css | Network | Corrected stylesheet path |
| 3 | Navigation used a div instead of nav | Accessibility tree | Changed div to nav |
| 4 | Heading jumped from h1 to h4 | Accessibility tree | Changed h4 to h2 |
| 5 | Image had no alt text | Lighthouse | Added descriptive alt |
| 6 | Label for="mail" did not match input id="email" | Lighthouse | Matched label and input |
| 7 | CSS used invalid property colour | Styles pane | Changed to color |
| 8 | Hover background declaration lacked a semicolon | Styles pane | Added semicolon |
| 9 | CSS selector .notes did not match HTML class .note | Styles pane | Corrected selector |
| 10 | Note text had insufficient contrast | Lighthouse | Changed text color to #595959 |

## Live site observations (Lab 4, Task 7)

### 1. Localhost vs live website
On localhost, I used HTTP and a local development server.
My published GitHub Pages website uses HTTPS, which encrypts
communication between the browser and the website.
The server and remote address are different because the
website is now hosted online instead of on my computer.

### 2. HTTPS certificate
The HTTPS certificate helps verify the website's identity
and enables encrypted communication.
Without HTTPS, someone on the same Wi-Fi network could
potentially intercept or modify unencrypted traffic.

### 3. localStorage
My saved orders from localhost did not appear on the live
website because localStorage is separated by origin.
The localhost address and GitHub Pages address are
different origins, so they have separate stored data.

### 4. Missing page
A page that does not exist returns HTTP status code 404.
On the published website, this response is served by
GitHub Pages rather than my local development server.

## CSS Specificity (Lab 4)

CSS specificity determines which style is applied when multiple rules target the same element.

An ID selector has higher specificity than a class selector, and a class selector has higher specificity than an element selector.

For example, #main has higher specificity than .container, while .container has higher specificity than main.

When two selectors have equal specificity, the rule written later in the stylesheet usually wins.
