Tricky layout cases can be described as equations.

```swift
button.CenterY == avatar.Bottom - 4
label.Width <= button.Width * 3
label.Height == (button.Width / 7) + 3
button.Left >= image.Right - 20
image.Height >= 100
view.Top == 10
```

The result is a native NSLayoutConstraint. So you can modify priority like so :

```swift
(label.Width == button.Width * 3).priority = 1000 // Making this a required constraint.
```
