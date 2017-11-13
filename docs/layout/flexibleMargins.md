Flexible margins can be used exactly like regular margins:

### With chainable Api

```swift
view.top(<=5)
view.left(>=20)
view.bottom(<=10)
view.right(<=15)
view.width(>=45)
view.height(<=100)
```

### In layout calls

```swift
layout(
    5,
    |-label-(>=5)-|,
    >=20,
    separator ~ (>=10),
    0
)
```
