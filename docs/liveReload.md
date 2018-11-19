# Live Reload

You can even enable **live reload** during your development phase! 🎉🎉🎉

Stevia + [InjectionForXcode](http://johnholdsworth.com/injection.html) = <3 (WhoNeedsReactNative??) 🚀

![Output sample](http://g.recordit.co/i6kQfTMEpg.gif)

*Just Cmd+S and you can dev live in the simulator !*

- Download [InjectionForXcode](http://johnholdsworth.com/injection.html) on the  [Appstore](https://itunes.apple.com/fr/app/injectioniii/id1380446739?l=en&mt=12)
- Install it & Launch it.
- Choose `Open Project` and choose your project's root folder.
- Make sure on  `File Watcher` is selected that Cmd+S triggers an injection.
- In your `AppDelegate`, put the following snippet to load injection on App start. Make sure to remove this for release builds :)

```swift
Bundle(path: "/Applications/InjectionIII.app/Contents/Resources/iOSInjection10.bundle")?.load()
```

In order to support **live reload** with InjectionForXcode, we simply need to tell our ViewController to rebuild a view after an injection occured.

in `viewDidLoad()` add :
```swift
on("INJECTION_BUNDLE_NOTIFICATION") {
    self.view = MyView()
}
```

And Voila :)
