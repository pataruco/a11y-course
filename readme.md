# Web Accessbility course

## Day 1

* Web (wrongly) is treated as graphic medium
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

* Use [pa11y](https://github.com/pa11y/pa11y) conformance report
