# Live Reload

You can even enable **live reload** during your development phase! 🎉🎉🎉

Stevia + [InjectionForXcode](http://johnholdsworth.com/injection.html) = <3 (WhoNeedsReactNative??) 🚀

![Output sample](http://g.recordit.co/i6kQfTMEpg.gif)

*Just Cmd+S and you can dev live in the simulator !*

- Download [InjectionForXcode](http://johnholdsworth.com/injection.html).
- Install it & Launch it.
- Restart Xcode.
- Click on  `Inject Source` once.
- Enable the `File Watcher` so that Cmd+S triggers an injection.

In order to support **live reload** with InjectionForXcode, we simply need to tell our ViewController to rebuild a view after an injection occured.

in `viewDidLoad()` add :
```swift
on("INJECTION_BUNDLE_NOTIFICATION") {
    self.view = MyView()
}
```

Currently InjectionForXcode doesn't seem to swizzle `init` methods for some reason. So we have to move our view code in another methods
```swift
convenience init() {
    self.init(frame:CGRect.zero)
    //View code
}
```
Becomes
```swift
convenience init() {
    self.init(frame:CGRect.zero)
    render()
}

func render() {
  //View code
}

```

And Voila :)
