# MooPopstateHashing

MooPopstateHashing is a simple wrapper that combines the HTML5 popstate, onhashchange and regular URL-changing techniques all into one.

Depending on which browser is using the tool, the appropriate technique will be used.

A data parameter is provided which can be used to set custom data to be transfered between pages.

## Browser Support

- Chrome, Safari, Opera, IE10+ and Firefox 4+ will use the HTML popstate technique. Only these browsers can see the data hash on back and forth operations.
- IE8, IE9 and all other browsers will use the hashbang technique.
- IE6 and IE7 and all other browsers that do not support the onhashchange event will use regular page redirects with window.location="..."

## Requirements

- MooTools Core 1.3+ (1.2+ works as well)

## Usage

All the functionality is mapped to two functions:

```javascript:
window.addEvent('addressChange',function(url,data) {
  alert(url); //new URL
});

window.setAddress(url); //set it to the new url
```
