```swift
sv(
    subview1,
    subview2,
    subview3
)
```
`sv([])` and `sv()` are essentially shortcuts that call `addSubview()` and
`view.translatesAutoresizingMaskIntoConstraints = false`

It also has the benefit of being **very visual** so that your can actually **see** what the view hierarchy is.
This is especially true for nested hierarchies :

```swift
sv(
    subview1,
    subview2.sv(
        nestedView1,
        nestedView2̨
    ),
    subview3
)
```
