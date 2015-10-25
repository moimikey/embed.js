##Dependencies

* Jquery >= 1.2
* [Highlight.js](https://highlightjs.org/) (Optional if code syntax highlighting is needed)
* [Twitter widgets.js](http://platform.twitter.com/widgets.js) (Optional if tweet embed support is set to true needed)

##Installation

Before installation, let me tell you that the dependencies other than jQuery are optional. In case, you haven't installed them make sure that you
turn off the respective features in the options.

Install through Bower

```shell
bower install --save embed-js
```

Install through npm

```shell
npm install --save embed-js
```

Loading the CSS

```html
<link rel="stylesheet" href="path/to/jquery.embed.css"/>
```

Loading the scripts

```html
<script src="path/to/jquery.min.js"></script>
<!--==== Optional =====-->
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/8.4/highlight.min.js"></script>
<script src="http://platform.twitter.com/widgets.js"></script>
<!--===================-->
<script src="path/to/jquery.embed.js"></script>
```

##Browserify Support

This plugin is [UMD](https://github.com/umdjs/umd) compatible so you can use it with browserify.

```javascript
var jquery = require('jquery');
require('embed-js');

jquery('#element').embedJS({
    gdevAuthKey : 'xxxxxxxx'
});
```






