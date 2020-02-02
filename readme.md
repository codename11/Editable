## Simple script for making text nodes editable

### Setup:
 - Include it in your document where parkup is.
 - Add `onload="Editable()"` in your body tag.

### How it works

 - Function `getSelector()` gets clicked element's absolute selector just like getting it from browser when you inspect element.

 - Function `getSelector()` gets called inside `Editable()` which have click listener inside, whom then passes it listeners event. 

 - `getSelector()` then finds all elements needed to traverse to get to wanted element. These get filtered through to create "selector" which is used to target partucular element and set it's contentEditable attribute to true.
 
 - Targeting particular element works however markup is structured.