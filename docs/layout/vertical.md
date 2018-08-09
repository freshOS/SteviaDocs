```swift
avatar.top(50)
```
==
```swift
layout(
    50,
    avatar
  )
```

While using `layout` for a single element might seem a bit overkill, it really **shines** when **combined with horizontal layout.**
Then we have the full **layout in one place** (hence the name).

```swift
layout(
    50,
    |-15-avatar.size(60)
  )
```
*The avatar is 50px from the top with a left margin of 15px and a size of 60px*

Another great example is the login view, representable in **one** single statement !

```swift
layout(
    100,
    |-email-| ~ 80,
    8,
    |-password-| ~ 80,
    "",
    |login| ~ 80,
    0
)
```

##### Chainable Api

The avatar example above could've been written that way using the chainable api :
```swift
avatar.top(50).left(15).size(50)
```

Using `layout` is just clearer in most of the cases but it's yours to choose which way you prefer :)
