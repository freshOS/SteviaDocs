Horizontally
```swift
alignHorizontally(avatar,name,followButton)
```

Vertically
```swift
alignVertically(title,subtitle,text)
```

Tops
```swift
alignTops(title,subtitle,text)
```

Bottoms
```swift
alignBottoms(title,subtitle,text)
```

Rights
```swift
alignRights(title,subtitle,text)
```

Lefts
```swift
alignLefts(title,subtitle,text)
```

Align the center of one view with another one :
```swift
alignCenter(view1, with: view2)
```


In the example above of a follow Cell, here is how the layout code would look like :
```swift
|-avatar-15-name-20-followButton-|
alignHorizontally(avatar,name,followButton)
```
But `|-avatar-15-name-20-followButton-|` actually **returns the array of views!!!** so we can write it in one **single** statement :

```swift
alignHorizontally(|-avatar-15-name-20-followButton-|)
```

Baselines

```swift
align(lastBaselines: label, label2, label3)
```

```swift
label.LastBaseline == label.LastBaseline + 24
```

🎉🎉🎉
