# Class 1

Objective-C

\* = pointer to object in memory
@ = used to signify a string in ObjC

layout code trumps storyboard?
- not sure if that's completely accurate.

Storyboard points to header file
- ?
Storyboard loads in full at launch
- you can programmatically generate views to reduce the numbers of view that pre-load
- or you can switch to multiple storyboards from the default main board

model view controller
- controller sits in-between the m and v

# Class 3

"unsigned" int meaning no negative sign - 
- int will always be positive if stored as unsigned
- allows for more storage

NSLog(@"my float is %f and %i", x, y);
- the %f or %i indicate the type of the var to put in the string. The trailing variables are the order in which to match to those types inline with the string.

## Methods
Method in ObjC means "send a message"
- (void)viewDidLoad {} is an early example of a method to UIKit
- (IBAction)myTestMethod:(id)sender {}
-- (id)sender is what we want to send into the IBAction method
- (void) = the return value
-- we could specify a return type or a var or whatever, but "void" sends back a message that the method has completed running.

(void)myVoidMethod:(float)myVariable
^ return  ^ Method  ^ input type  ^ input 

variables created within a method are only asseccible within that method. 

- (void) myVoidMethod:(float)myFloat multiplier:(int)myMultiplier {}
                        label for 2nd arg ^              ^ arg name
- the first argument in doesn't get the convience of a label
- popup tooltip shows the label you give to arguments after the first

NSObject = highest level object in ObjC
- strings, views, etc are all subclasses of NSObject

Started "CreatingObjects" project

\* pointer in memory
UILabel *myLabel = [[UILabel alloc] init];
alloc = "hey, set aside some memory for this."

[self.view addSubview:myLabel];
- passing in the object myLabel, not just the value of view.

Hierarchy
NSObject > UIViewController > myViewController > viewDidLoad or myOwnMethod

NSNumber is an object. 
%@ is for strings that reference an object
%f = float

Expanding NSArray topic

Code Signing
Provisioning Profile
- set to specific if you have issues with the automatic settings.

## Assignment
Coming via email.