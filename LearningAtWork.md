fpo = for placement only

clip subviews
- helps with autolayout

sort order of layers in outline effect view priority in IB 
- just like Photoshop

"Aspect Fill" to leave ratio of image untouched

NIB vs XIB
- XIB is in XML

console rm -Rf = remove recursively and force it.
- be careful bro. This could be pretty negative.

Optional chaining?

Changing TextView
- aligning
-- text doesn't align on the left edge, it's aligning based on the TextView left bound.
--- Common offset?
- background color
-- currently black? Where is that controlled?
- shift view with keyboard
-- http://stackoverflow.com/questions/25693130/move-textfield-when-keyboard-appears-swift
-- http://www.raywenderlich.com/77092/text-kit-tutorial-swift
- multiline wrap?

1. Layout 80% of issues on next screens [x] []
2. Address flow between screens? [] []
3. TextView respond to keyboard [] [] []

Alignment constraint ratio has to be anchored to something where a ratio makes sense - center Y in superview is an example, compared to anchored to the top of the superview.
- to split two buttons 50/50 at the bottom, tied left to left edge and then for width constrained to superview center X and set the ratio to 2:1. Then for the button on the bottom right, set to equal width as other button and set to trailing left edge = 0.

Overlay modal view
http://mathewsanders.com/custom-menu-transitions-in-swift/