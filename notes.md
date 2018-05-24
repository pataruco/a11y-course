# Web Accessbility

* Design for the lowest group
* Web (wrongly) treated as graphic medium
* Graphic design has dominated Web design. is it Web design is related to Graphic design?
* `display:none` disable sounds
* text browser -> [lynx](<https://en.wikipedia.org/wiki/Lynx_(web_browser)>)
* Colour blindness, the less considered kind of disability
  * if your design works in monochrome it's accessable
* Always support keyboard interface
* Redundancy on techniques is key
* Think about people with mild disabilities (elderly people)
* If you cannot navigate a website on text browser (lynx) if possible is not accessible
* Just make the code accessible for screen reader, because it's impossible to give support to all assitance technologies
* The input of a screen reader is the output of every browser, so the experience is different per browser
* Enable with JS form filling, but always set a fallback
* `longdesc` give a URL to a description, but it's been [obsolete](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#attr-longdesc) on `aria-describedby` or `aria-details`.
* `itemscope` `itemtype` from [Schema.org](http://schema.org/)
* [pa11y](https://github.com/pa11y/pa11y) a good CLI tool for a11y automating test
* [Wave](http://wave.webaim.org/)
