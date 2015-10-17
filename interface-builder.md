#Interface Builder  

Interface Builder (IB) provides developers a way to build out the user-interface without writing any code. Developers can accomplish everything in code, however Interface Builder provides quick and visual shortcuts for UI design.

###Assistant

###Storyboards
Introduced in iOS 5, Storyboards allow developers to design entire workflows.

###Autolayout
One of the power features delivered in iOS 6 is Autolayout; a relation-based dynamic runtime positioning system for views. Prior to iOS 6, developers used Springs and Struts however this was limited in its capabilities and often required developers to write code to manually position even moderately complex view layouts.

###Size Classes
As a way of handling the growing divergence in screen sizes, Apple introduced Size Classes in iOS 8. Constraints can be enabled or disabled on a per-size-class basis to achieve specialized layouts for certain screen sizes without having to create multiple versions of the same storyboard or Nib for each screen size.

Screen Dimensions are broken down into "Compact" and "Regular" along both Horizontal and Vertical axes. If constraints should be enabled in both "Compact" and "Regular" Size Classes, then "Any" can be used.

###Utilities
When using Interface Builder, the Utilities panel on the right-hand side displays specialized Inspector tabs for manipulating IB content. Besides the normal "File" and "Quick Help" Inspector, below are the 4 tabs that become visible in IB and a short description of each one.

#####Identity Inspector


#####Attributes Inspector

#####Size Inspector

#####Connections Inspector
