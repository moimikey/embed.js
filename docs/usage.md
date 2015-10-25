For the plugin to work, you will have to follow a particular HTML structure but hey you can even configure it .

##Basic Usage

```html
<!--======== HTML Structure ==========-->
<div id="element">
  <div> Some content here </div>
  <div> Some content here </div>
  ...
  ...
</div>

<!--======== Calling embed.js ========-->
<script>
$('#element').embedJS({
    gdevAuthKey   : 'xxxxxxxx'
});
</script>
```

But wait how the hell are you going to use it with so many nested `div` present in your code. Chill out! We have got you covered there.
Configure it according to your needs by giving a class to the child elements . 

```html
<!--========= Custom HTML Structure ==========-->
<div id="element">
    <span> Some content here </span>
    <span> Some content here </span>
</div>

<!--====== calling embed.js with setting custom selector ======-->
<script>
$('#element').embedJS({
    embedSelector : 'span',      
    gdevAuthKey   : 'xxxxxxxx'
});
</script>
```