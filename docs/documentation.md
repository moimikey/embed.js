#Advanced Options
---

```xml
<script>
$('#element').embedJS({
      embedSelector   :'div',
      link              : true,
      linkTarget        : '_blank',
      linkExclude       : ['jpg','pdf'],
      docEmbed          : true,
      docOptions        : {
              viewText    : '<i class="fa fa-eye"></i> View PDF',
              downloadText: '<i class="fa fa-download"></i> DOWNLOAD'
      },
      imageEmbed        : true,
      imageLightbox     : true,
      audioEmbed        : false,
      videoEmbed        : true,
      basicVideoEmbed   : true,
      videoWidth        : 640,
      videoHeight       : 390,
      gdevAuthKey         : 'xxxxxxx',
      locationEmbed       :true,
      mapOptions        : {
            mode: 'place'                   
      },
      highlightCode     : true,
      tweetsEmbed     : true,
      tweetOptions    : {
            maxWidth   : 550,
            hideMedia  : false,
            hideThread : false,
            align      : 'none',
            lang       : 'en'
      },
      excludeEmbed     :['twitchTv'],
      codeEmbedHeight  :300,
      soundCloudOptions: {
          height      : 160,
          themeColor  : 'f50000',    //Hex Code of the player theme color
          autoPlay    : false,
          hideRelated : false,
          showComments: true,
          showUser    : true,        //Show or hide the uploader name, useful e.g. in tiny players to save space)
          showReposts : false,
          visual      : false,       //Show/hide the big preview image
          download    : false        //Show/Hide download buttons
              },
      vineOptions:{
            maxWidth:null,
            type:'postcard',         //'postcard' or 'simple' embedding
            responsive:false         // whether to make the vine embed responsive
      },
      //callback before doc preview
      beforeDocPreview  : function(){},
      //callback after doc preview
      afterDocPreview   : function(){},
      // callback on video frame view
      onVideoShow:function(){},
      //callback on video load (youtube/vimeo)
      onVideoLoad:function(){}
      //function to execute before embedding services
      beforeEmbedJSApply: function () {},
      //callback after embedJS is applied
      afterEmbedJSLApply: function () {},
      //callback after the twitter widgets of a BLOCK are loaded.
      onTwitterShow     : function () {}

});
</script>
```

<h3>gdevAuthKey</h3>

  option|default value|usage
-----------|---------------------|----------
gdevAuthKey|null|( Mandatory ) The authorization key obtained from google's developer console for using youtube data api and map embed api

The steps of obtaining the gdevAuthKey are mentioned [here](https://developers.google.com/api-client-library/python/guide/aaa_apikeys)

<h3>embedSelector</h3>

  option|default value|usage
-----------|---------------------|----------
embedSelector|'div'|The selector(id/class/tagName) inside #element that needs to be processed  

<h3>link</h3>

  option|default value|usage
-----------|---------------------|----------
link|true|Instructs the library whether or not to embed urls

<h3>linkTarget</h3>

  option|default value|usage
-----------|---------------------|----------
linkTarget|'_blank'|same as the target attribute in html anchor tag . supports all html supported target values.

<h3>linkExclude</h3>

  option|default value|usage
-----------|---------------------|----------
linkExclude|[]|Array of extensions to be excluded from converting into links

<h3>docEmbed</h3>

  option|default value|usage
-----------|---------------------|----------
docEmbed|true|set false to show a preview of document(pdf,xls,xlsx,doc,docx,ppt) links

<h3>docOptions</h3>

  option|properties|default value|use
-----------|---------------------|----------|---
docOptions
|viewText    | '&lt;i class="fa fa-eye"&gt;&lt;/i&gt; View PDF'|kjljk
|downloadText| '&lt;i class="fa fa-download"&gt;&lt;/i&gt; DOWNLOAD'|ljklj

<h3>imageEmbed </h3>

  option|default value|usage
-----------|---------------------|----------
imageEmbed|true|set false to disable embedding images


<h3>imageLightbox</h3>

  option|default value|usage
-----------|---------------------|----------
imageLightbox|true| set true to enable lightboxes for images

<h3>audioEmbed</h3>

  option|default value|usage
---|---|---
audioEmbed|false|set to true to enable audio embedding

<h3>videoEmbed</h3>

option|default value|usage
---|---|---
videoEmbed|true|set true to show a preview of youtube/vimeo videos with details

<h3>basicVideoEmbed</h3>

option|default value|usage
---|---|---
basicVideoEmbed|true|set true to show basic video files like mp4 etc. (supported by html5 player)

<h3>videoWidth</h3>
option|default value|usage
---|---|---
videoWidth|640|width of the video frame (in px)

<h3>videoHeight</h3>
option|default value|usage
---|---|---
videoHeight|390|height of the video frame (in px)

<h3>locationEmbed</h3>

option|default value|usage
---|---|---
locationEmbed|true|Set google map location embed. Use @(place-name) to use this feature . Eg: `@(Sydney)`

<h3>mapOptions</h3>

  option|properties|default value|use
-----------|---------------------|----------|---
mapOptions
|mode|'place'|'place' or 'streetview' or 'view'

<h3>highlightCode</h3>

option|default value|usage
---|---|---
highlightCode|true|Instructs the library whether or not to highlight code syntax.

<h3>tweetsEmbed</h3>

option|default value|usage
---|---|---
tweetsEmbed|true|Instructs the library whether or not embed the tweets


<h3>tweetOptions</h3>
  option|properties|default value|use
-----------|---------------------|----------|---
tweetOptions
|maxWidth|500|The maximum width of a rendered Tweet in whole pixels. Must be between 220 and 550 inclusive.
|hideMedia|false|When set to true or 1 links in a Tweet are not expanded to photo, video, or link previews.
|hideThread|false|When set to true or 1 a collapsed version of the previous Tweet in a conversation thread will not be displayed when the requested Tweet is in reply to another Tweet.
|align |'none'|Specifies whether the embedded Tweet should be floated left, right, or center in the page relative to the parent element.Valid values are left, right, center, and none. Defaults to none, meaning no alignment styles are specified for the Tweet.
 |lang |'en'|Request returned HTML and a rendered Tweet in the specified. Supported Languages listed here [https://dev.twitter.com/web/overview/languages](https://dev.twitter.com/web/overview/languages)

<h3>excludeEmbed</h3>

option|default value|usage
---|---|---
excludeEmbed|[]|An array of services excluded from embedding...Options : codePen/ jdFiddle/ jsBin/ ideone/ plunker/ soundcloud/ twitchTv/ dotSub/dailymotion/ vine/ ted/ liveleak/ spotify/ ustream/ flickr/ instagram. Can exclude all options by setting it to `'all'`

<h3>codeEmbedHeight</h3>

option|default value|usage
---|---|---
codeEmbedHeight|300|Height of jsfiddle/codepen/jsbin/ideone/plunker in pixels

Only `gdevAuth` option is mandatory. Other options provide you additional control on the plugin.



If you specify either one of **videoWidth** or **videoHeight** , the other option will be automatically set in the aspected ratio.

<style>
  table{
    width: 100%;
  }
  </style>