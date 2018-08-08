Width
```swift
view.width(100)
```

Height
```swift
view.height(100)
```
`view ~ (100)` is same with `view.height(100)`

You can use `~` operator for `.height(x)`. It's just more readable in a layout statement that way.

Size
```swift
view.size(100)
```

Constraining multiple views
```swift
equalSizes(image1, image2, image2)
equalWidths(field1, field2, field3, field4)
equalHeights(button1, button2)
```

Constraining a view to stay squared
```swift
view.heightEqualsWidth()
```
