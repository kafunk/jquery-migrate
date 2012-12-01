# jquery-compat: Restore deprecated features for jQuery 1.9+

This project includes APIs, features or functionality that have been deprecated in jQuery and removed as of version 1.9. They include:

* `jQuery.browser` [docs](http://api.jquery.com/jquery.browser)
* `jQuery.sub` [docs](http://api.jquery.com/jquery.sub)
* `jQuery.fn.toggle` [docs](http://api.jquery.com/toggle-event/) (event click signature only)
* `jQuery.fn.data` data events (undocumented)
* `"hover"` pseudo-event name []()
* `jQuery.fn.error` [docs]()
* `ajaxStart, ajaxSend, ajaxSuccess, ajaxError, ajaxComplete, ajaxStop` global events on non-`document` targets [docs]()
* `jQuery.attrFn` object (undocumented)

In your web page, make sure to load this plugin *after* the script for jQuery:

```html
<script src="jquery.js"></script>
<script src="jquery-compat.js"></script>
```

### Development version

This version provides console warning messages when deprecated and/or removed APIs are used. In browsers that don't support the console interface such as IE7, no messages are generated unless you include a debugging library such as [Firebug Lite](https://getfirebug.com/firebuglite). Use this version during development and debugging, and whenever you are reporting bugs.

*Latest released development version:* This file is hosted on jQuery's CDN, and can be hotlinked if desired.
[http://code.jquery.com/jquery-compat-0.0.0.js](http://code.jquery.com/jquery-compat-0.0.0.js)

*Current work-in-progress build:* Although this file represents the most recent updates to the plugin, it may not have been thorougly tested.
[https://raw.github.com/jquery/jquery.compat/master/dist/jquery-compat.js](https://raw.github.com/jquery/jquery.compat/master/dist/jquery-compat.js)

### Production version

The minified production file is compressed and does not generate console warnings.  Do not use this file for development or debugging, it will make your life miserable.

Latest released development version: 
[jquery-compat-0.0.0.min.js](http://code.jquery.com/jquery-compat-0.0.0.js)

*Current work-in-progress build:* Although this file represents the most recent updates to the plugin, it may not have been thorougly tested. We do not recommend using this file on production sites since it may be unstable; use the development versions above.
[jquery-compat.min.js](https://raw.github.com/jquery/jquery.compat/master/dist/jquery-compat.min.js)

## Reporting problems

Any bugs should be reported on the [jQuery Core bug tracker](http://bugs.jquery.com) and *must* be accompanied by an executable test case that demonstrates the bug. The easiest way to do this is via an online test tool such as [jsFiddle.net](http://jsFiddle.net) or [jsbin.com](http://jsbin.com).


How to run the tests:
====================================================
Clone this repo, install `grunt`:

```sh
git clone git://github.com/jquery/jquery-browser.git
cd jquery-browser
npm install -g grunt
```

Run `grunt` to `lint`, `test` and `min` release.

```sh
grunt
```

