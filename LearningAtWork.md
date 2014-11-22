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

# 11/13/14
Trying to get the text fields to move up once the keyboard has been activated.

Easy menu option to embed all the selected views within a scrollview.
- http://stackoverflow.com/questions/16956893/moving-subviews-from-one-view-to-another-view-without-changing-any-position-info

How do I set constraints for items within a scroll view?
- http://www.twistedape.me.uk/blog/blog/2014/09/08/horizontal-paging-scroll-view-with-varying-width-in-storyboards/
-- that's for side scrolling screens. Doesn't really answer the basic question of the order of constraints - the hierachy of what's related to what in a scroll view.

? after the type means the var is of an optional type. Basically, means it can be nil AKA nothing.
? after the variable then that means it could be nil, and if so, don't do the thing you're trying to do.
! after variable name means, this var could be nil, we don't expect that, but if it is crash.

as? type  - means try to treat this as this type. 

po __some object__
- way to print objects in the debugger

Put a subview frame within the tab buttons and change it to the project (orange) color when someone touches it.
- also, try to adjust the layout of the four buttons so they don't hang off the edge.

BDTabButton

if line.superview != self {
	addSubview(line)
}

var frame = CGRect(x: 0, y: bounds.height-3, width: bounds.width, height: 3)

self.addSubview(UIView(frame: frame))

layoutSubviews get called twice 
- when created
- if resized

Adding labels that update based on the values from the data model.
- counts for each tab
- where are the labels getting built / updating their text
-- the labels are named in UserProfileHeaderVC
-- the styling takes place in the class TabButton

Visual Layout Language
http://makeapppie.com/2014/07/26/the-swift-swift-tutorial-how-to-use-uiviews-with-auto-layout-programmatically/

# 11/17

fixed layout. Constraints were set to ratios instead of fixed H and W for the image.
~~Text overrun past table view.~~

~~Once image swaps, touch events don't work?~~
~~- disable user interaction on button to see if it passes through to the cell.~~

~~location name falls off the screen. 
- auto ellipsis?~~

~~Register screen
- rebuild constraints~~

# 11/18

Think of optional types like an alpha channel in video. 
RGB -> RGB+A // works
RGB+A -> RGB // you lose the alpha channel

String -> String?
String? -> String // loses the optional information 

Optional bit basically says, "Does this exist?" true or nil.

---
Best ways to handle scalable graphics in Xcode
- http://martiancraft.com/blog/2014/09/vector-images-xcode6/
-- create PDF's that generate all 3 sizes at build time.
-- negatives: "This is not full vector support — PNG images are generated at build-time, and you maintain no control over this."
-- "You cannot choose a new size for the image once you’ve specified to use the vector-scaled image in your app. Stick with the size you’ve specified, or create a new PDF for the larger size. Otherwise, the images will be distorted if you scale with AutoLayout, for instance."

- http://www.smashingmagazine.com/2012/12/03/design-ios-apps-with-adobe-fireworks/
-- Adobe Fireworks

layout login and reg screens

