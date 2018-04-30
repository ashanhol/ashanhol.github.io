# Progress Log

## Issues

### Individual Posts
* Fruit Warrior
    * Check all the Code sections and the use of {{site.url}}
        * Also for general issues
    * Images need captions
    * Solved Numbered Lists issue (images break list count) by replacing them with h3 tags
* Five Steps to VR Game
    * Solved Numbered Lists issue (images break list count) by replacing them with h3 tags
* PAX - the screenshot of the crowd isn't available anymore
    * Should I just make a "this image is no longer available" .png file?

## CSS Thoughts
* Defense Brigade pt 2 and other posts with long lines of code: Is it possible to have the code word wrap?
    * Simple fix via sass/css - see [here](https://david-kerwick.github.io/blog/blogger/2015/07/24/wrapping-code-jeykll-pygments.html)
    * simplest fix is to add `pre { white-space: pre-wrap; }`
