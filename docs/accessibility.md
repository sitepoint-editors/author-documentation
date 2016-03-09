# Accessibility Guidelines

Some guidelines for making example code as accessible as possible.

##1. HTML Should be Semantic
"Semantic" here means two things:

 - Using the right tag for the content. Headings for headings, lists for lists, buttons for things that 'Do Stuff' on the page and anchors for things that navigate users somewhere, etc.
 - Fallbacks. If you're building a component/widget and something breaks then ideally your component should either *not render* or *render as something sensible*.

HTML should be valid. If it's not, check if it's got a _legitimate_ reason not to be valid (if you're using custom attributes, be safe and throw `data-` in front of it.)

##2. Device input agnosticism!
Make sure your app/component can be used sensibly with at least:

  - touch
  - keyboard
  - mouse.

Keyboard functionality is mostly accomplished by step 1 (use the correct HTML), which gets you a lot of the necessary functionality for free.
For widgets, there may be a prescription of which keyboard actions should do what. Check this page https://www.w3.org/TR/wai-aria-practices/#aria-ex and see if your widget falls into any of the categories there.

##3. Visual Focus
For keyboard users, make sure visual focus is a thing. People need to see where they are. Often you've already got a `:hover` style. Add the `:focus` line to it, done.

##4. Focus Management
Make sure when your widget 'Does Stuff', focus can't get lost.

Examples:

- User triggers a modal-anything. The focus should not be able to leave a modal until the user has either done the task involved, or closed the modal (ESC should always be able to close something like a modal or a popup). Focus should wrap around (forwards AND backwards) inside the modal.
- When the object being focused on vanishes (the user closed the modal; the user clicked a Delete button and now the button and item are both gone), move the focus with JavaScript to the next obvious place.
- Focus needs to follow the visual layout. Normally this just happens naturally on a page, and you should mostly be getting this for free because you followed Rule 1 and have a sensible content order. If you need to control the focus order because of the funkiness of your widget, it's preferable to do that with JS setting focus() rather than setting positive tab indices.

##5. Label Stuff
- Put the lang attribute on the `<html>` tag.
- Have a useful `<title>` for the page. Making an SPA? Change that as the view changes to reflect the current page.
- All form controls should have labels. No, the first option of a `<select>` tag or similar is not a label -- the first option is the first option. So add a label. Use the for attribute. If the design calls for no labels, then hide it offscreen or clip it.

##6. No Auto-play
This goes for videos, decorative-background videos, carousels, and even for transition events. Easiest is to let the user turn it off (and in a super-obvious way).

##7. Don't Jerk People Around (Literally)
 Moving to somewhere else needs to be obvious and generally caused by the user doing an action (they clicked a link, they submitted a form, etc). Things users don't expect to jerk them over to some amazing new context include hovering, focusing, scrolling, or tabbing.

##8. ARIA
The first rule of ARIA is: don't use ARIA. Use semantic HTML elements whenever possible. Wrong/incorrect use of ARIA is often more damaging than not using it at all.
The second rule of ARIA is: don't override existing roles. HTML elements (in modern browsers anyway) have native, built-in "roles". Don't do `<a href="foo" role="link">blah</a>`, and don't do `<h2 role="button">click me</h2>`.