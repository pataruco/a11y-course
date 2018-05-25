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

* Suggest RB to use [pa11y](https://github.com/pa11y/pa11y) to write automated conformance reports
* Use `aria-describedby` and `aria-labelledby` with a value of an id and the SR will read the content
* Use `aria-live` when we _live regions_ are on the page
* `role=alert` is always used an `assertive` instead a `polite` `aria-live`
* `role=alertdialog` must have `aria-labelledby` or `aria-label`
  * Must be a modal to break the flow of the SR.
* if you use a `<canvas>` use `role=application`
* To use `tabindex` is ok, but if you found using it, first think to change the source order of your HTML
