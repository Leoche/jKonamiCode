<p align="center">
<img src="./jkonamicode.png">
</p>

## Installation
#### 1. First include jQuery before `</body>`
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js" type="text/javascript"></script>
```

#### 2. Include jKonamiCode.js
From release
```html
<script src="jKonamiCode.js" type="text/javascript"></script>
```
Or from CDN hosted by [jsDelivr](https://www.jsdelivr.com/)
```html
<script src="//cdn.jsdelivr.net/gh/Leoche/jKonamiCode@1.0.0/jKonamiCode.js" type="text/javascript"></script>
```
#### 3. Initialize the plugin
```html
<script type="text/javascript">
    (function($){ // Waiting for jQuery to load
        $(window).jKonamicode(function(){
            // Executed when Konami code is entered
            alert("My super easter egg");
        });
    })(jQuery);
</script>
```

## Customization
This plugin comes with a event function triggered when a right key `onRightKey()` is detected and have one args which is the number or right keys entered.
You can also change the keyCodes if you want to have a custom code scheme.
```javascript
(function($){
  $(window).jKonamicode({
    {code:[38,38,40,40,37,39,37,39,66,65], // Konami Code
    onRightKey:function(e){
        alert("You entered "+e+" right keys.");
    }},
     function(){ // Success function
        alert("You just entered the entire konami code!");
     }
  );
})(jQuery);
```
Here is a table of all chars keyCodes: [keyCodes Table](https://www.cambiaresearch.com/articles/15/javascript-char-codes-key-codes)