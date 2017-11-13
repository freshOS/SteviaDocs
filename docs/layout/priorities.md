There is no special Stevia api for priorities.
In order to set them, you need to use the good'ol standard api :)
By default, Stevia constraints are created with a priority of **751**.

```swift
let c = NSLayoutConstraint(item: v, attribute: .Top, relatedBy: .Equal, toItem: v, attribute: .Top, multiplier: 1, constant: 0)
c.priority = 1000 // Make a constraint `required`
addConstraint(c)
```

```swift
(label.Width == button.Width * 3).priority = 1000 // Making this a required constraint.

let constraint == view.Height = 50 % Height
// later..
constraint.priority = 750
```
