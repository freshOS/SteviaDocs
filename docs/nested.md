We believe complex nested views should be refactored into their own `UIView` subclasses.

For instance, if out App is using a form field multiple times, it is wise to extract it in its own UIView subclass like so:



```swift
class CustomField: UIView {

    let icon = UIImageView()
    let field = UITextField()
    let image = UIImageView()

    convenience init() {
        self.init(frame:CGRect.zero)

        sv(
            icon,
            field,
            image
        )

        alignHorizontally(|-icon.size(40).centerVertically()-field-image.size(40)-|)

        backgroundColor = .whiteColor()
        layer.cornerRadius = 5
        layer.shadowOffset = CGSize(width: 2, height:2)
        layer.shadowOpacity = 0.5
        icon.backgroundColor = .grayColor()
        image.backgroundColor = .blackColor()
    }
}
```
And then we can use it easily like so whenever we need it:
```swift
class LoginView: UIView {

    let usernameField = CustomField()
    let passwordField = CustomField()
```
