# High Performance in the Critical Rendering Path
*Nicolás Bevacqua* [@nzgb]()

* [Pony Foo](ponyfoo.com)

---

## Measure
* DevTools Audits
  * Per resource advice
* PageSpeed Insights
  * Mobile, desktop
  * Get a rough score
  * Best practices
  * Practical advice
* WebPageTest
  * Makes it easy to spot FOIT
  * Calculates SpeedIndex
  * Inspect every request
  * Analyze TCP traffic
  * Identify bottlenecks
  * Visualize progress

## Automate
* npm  ```psi```
* npm  ```webpagetest-api```
* Yslow

## Budgets
* Enforce a performance Budgets
* Track impact of every commit
* npm ```grunt-perfbudget```

## Beyond minification
* Networking
  * **Book**: High Performance Browser networking - Ilya Grigorik
  * OPtimizing TCP
    * Increase initial TCP cwnd size
    * Disable slow-start restart (SSR) (should be enabled by default on server)
    * Turn on keep-alive
    * GZip all the text
    * Add Expires and Etag headers
    * Use a CDN
  * Optimizing HTML
    * Render server-side
    * Become a SPA later
    * Defer noncrit asset loading
    * Keep accessible with ARIA
  * Optimizing CSS
    * Inline crit CSS
    * Removed unused styles
    * Concat and minify
  * Optimizing Fonts
    * Load async
    * Use fallback
    * Prevent FOIT using JS
    * Use fewer fonts , avoid repaints
    * Cache aggressively
  * Optimizing JS
    * Defer all of it
    * Small modules

## How
* Use NGINX
* Set up a CDN
  * Cloudflare
* Defer assets
* Remove Unused CSS
  * npm ```gulp-uncss```
* Inline critical CSS
  * npm ```penthouse```
* Use a Font loader
  * npm ```fontfaceonload```
* Optimize Images
  * npm ```imagemin```
* Create spritesheets
  * npm ```spritesmith```
* Inline Images
 * npm ```datauri```
* Use a module system
  * Browserify
  * Babel
  * etc..
* Perfschool
