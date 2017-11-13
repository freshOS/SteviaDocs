Well, just call `style` on a UIView subclass :

**In-line** for small or unique styles

```swift
detail.style { l in
  l.numberOfLines = 0
  l.textAlignment = .Center
  l.textColor = .blueColor()
  l.text = NSLocalizedString("NeedPetMessage", comment: "")
}
```

Or in a separate to make them reusable

```swift
// My style method, kinda like CSS
func detailStyle(l:UILabel) {
  l.numberOfLines = 0
  l.textAlignment = .Center
  l.textColor = .blueColor()
  l.text = NSLocalizedString("NeedPetMessage", comment: "")
}

// Later
{
  // Set my style
  detail.style(detailStyle)
}
```

This is the **preferred** way because the styles become **reusable** and **composable**: you can chain them!
You can even create a Style File grouping high level functions for common styles.
Usage then becomes very similar to CSS!
