## Simple script for making text nodes editable

### Setup:
 - Include it in your document where markup is.
 - Add `onload="Editable()"` in your body tag.

### How it works

 - Function `getSelector()` gets clicked element's absolute selector just like getting it from browser when you inspect element.

 - `getSelector()` finds all elements needed to traverse to get to wanted element. These get filtered through to create "selector" which is used to target partucular element and return said `selector`. 
 - Targeting particular element works however markup is structured.
 ----
 - Function `Editable()` have series of event listeners which handle particular portion of a code: 
  1. First one is on click which gets clicked element and set its attribute `contentEditable` to true, also it passes it's value to `elm` variable which is then used in fourth event listener.
  2. Then there is a `mouseover` event which is used for highlighting targeted element.
  3. Third one removes everything that previous(`mouseover`) event did, when user moves cursor out of element.
  4. Last one is used that when user is done editing and by subsequently pressing `Esc` key, it ends it's editing session.