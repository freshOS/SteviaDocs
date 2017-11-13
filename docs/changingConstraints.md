After laying out a view once, how do I change some constraints ?

## Simple Changes

```swift
// Initial layout
image.height(100)

// And later on
image.heightConstraint?.constant = 200
```
Those getters are available for `left`, `right`, `top`, `bottom`, `height` and `width` constraints


## Complex changes
When we want to change the whole layout at once then the best strategy is to
flush & relayout.

```swift
// Initial layout
layout(
    100,
    |-email-|,
    8,
    |-password-|,
)

// Flush all view constraints
removeConstraints(constraints)

// Re-apply different layout
layout(
     |-password-|,
     8,
     |-44-email-100-|,
     10
 )
```  

## Animating Changes

To animate a constraint is to change the constant property on it and then call self.layoutIfNeeded() in an animation block.

Animating with stevia is no different than native Autolayout


In both cases, animating the constraint change is as easy as calling `layoutIfNeeded` in an animation block.

```swift
UIView.animateWithDuration(2) {
    self.layoutIfNeeded()
}
```
