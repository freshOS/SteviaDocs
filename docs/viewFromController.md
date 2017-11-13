Once again, this is not Stevia-related per se but since we're not generally used to writing views in code, then some explanation might be useful  🤓

It goes like this :  
- 1. Keeping a reference to our custom view.  
- 2. Loading our view instead of the bare default one by overriding `loadView`

```swift
class MyViewController: UIViewController {

    let myCustomView = MyCustomView() // 1

    override func loadView() { // 2
      view = myCustomView
    }

    override func viewDidLoad() {
        super.viewDidLoad()
        myCustomView.loginButton.addTarget(self, action: #selector(login), for: .touchUpInside)
    }

    @objc
    func login() {
      // do something
    }
}
```
