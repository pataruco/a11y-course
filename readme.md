# Web Accessbility course

## Day 1

* Web (wrongly) is treated as graphic medium
* Design always from the lowest denomination group
* `display:none` disable sounds
* Use text browsers to test a11y ([lynx](<https://en.wikipedia.org/wiki/Lynx_(web_browser)>))
* Colour blindness is the less considered kind of disability
  * if your design works in monochrome it's accessible
* Always support keyboard interface
* Redundancy on techniques is key
* Think about people with mild disabilities (elderly people)
* If you cannot navigate a website on text browser (lynx) is quite possible taht is not accessible
* Just make the code accessible for a screen reader, because it's impossible to give support to all assistance technologies
* The input of a screen reader is the output of every browser, so the experience is different per browser
* Enable JS form filling, but always set a fallback with vanilla HTML and server side validation
* `longdesc` give a URL to a description, but it's [obsolete](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#attr-longdesc), Use `aria-describedby` or `aria-details`.
* `itemscope` `itemtype` from [Schema.org](http://schema.org/) give microdata content to assistance technologies interfaces
* [pa11y](https://github.com/pa11y/pa11y) a good CLI tool for a11y automated test
* [Wave](http://wave.webaim.org/) is still well used

## Day 2

* Suggest to Red Badger to use [pa11y](https://github.com/pa11y/pa11y) to write automated a11y conformance reports
* Use `aria-describedby` and `aria-labelledby` with a value of an id and the screen reader (SR) will read the content
* Use `aria-live` when we _live regions_ are on the page
* `role=alert` is always used an `assertive` instead a `polite` `aria-live`
* `role=alertdialog` must have `aria-labelledby` or `aria-label`
  * Must be a modal to break the flow of the SR.
* Using [Aria](https://w3c.github.io/using-aria/)
* if you use a `<canvas>` use `role=application`
* To use `tabindex` is ok, but if you found using it, first think to change the source order of your HTML
  * the same of above with `accesskey`
* The MOST import thing to help navigation on single page is to have correct hierachy order on titles (`h1` to `h6`)
* Provide as many _HTML phrases_ as you can, e.g `em`, `strong`, `abbr`, `cite`, `blockquote`, `q`
* If you are using `em`, `strong` the SR is shouting to blind people.
* Never use HTML for styling purposes, e.g. use a `h3` to create a blockquote
* Don't stop the user to increase font sizes, so always use
  * ```css
    html {
      font-size: 1em; /* fallback for IE < 9 */
      font-size: 100%;
    }
    body {
      font-size: 100%;
    }
    ```
* Set different gradients or colours for `focus`, `active`, `focus`, `visited`
* Never require hovering to make links or actions visible
* If an image is not meaningful to explain the content, use the image as CSS `background-image` insted to HTML `img`
* `alt` describe function `title`describe content
* Use `alt` as fallback if image is not rendering
* is valid to have empty `alt` attributes if the information is redundant
* `title` also conveys to be supplemantary information
