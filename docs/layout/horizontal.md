This is intended to look like **Apple's visual format**, so you should be very familiar with the syntax.
Stevia only removes the `[]` and the String.

Stick a label to the left of the screen
```swift
|label
```

With the default margin (8)
```swift
|-label
```

With a custom margin
```swift
|-42-label
```

Just to be very clear we want to **emphasize** that this is **pure syntactic sugar**.
This equivalent of the following using the chainable api :

```swift
label.left(42)
```
Which in turn will create **Native Autolayout constraints** :
```swift
label.superview?.addConstraint(
  NSLayoutConstraint(
    item: label,
    attribute:.Left,
    relatedBy: .Equal,
    toItem: label.superview!,
    attribute:.Left,
    multiplier: 1,
    constant: 42
  )
)
```

Combine all at once.

```swift
|-avatar-15-name-20-followButton-|
```
