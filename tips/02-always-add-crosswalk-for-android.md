### Always add crosswalk for Android

As you know, Ionic is a hybrid platform that runs and depends heavily on native `WebView` on Android; however, there are so many Android version, and each version is shipped with different version of `WebView` that work differently, which makes app development on Android more difficult.

For that reason, [the Crosswalk project](https://crosswalk-project.org/) is initiated and under heavy development to provide the latest modern and stable Chromium browser for all Android devices, a web runtime actually. Some advantages quoted from the project website,

* Get consistent, predictable behavior by reducing Android device fragmentation.
* Use the latest web innovations and APIs. Provide a feature rich experience on all Android 4.0+ devices.
* Easily debug with Chrome DevTools.
* Improve the performance of your HTML, CSS, and JavaScript.

It's great, isn't it? Less troubles when dealing with inefficiency on Android devices. [Ionic official documentation](http://ionicframework.com/docs/cli/browsers.html) also suggests to add Crosswalk browser for Android, so you should do it.

To see the list of available browser:

```
$ ionic browser list

iOS - Browsers Listing:

Not Available Yet - WKWebView
Not Available Yet - UIWebView


Android - Browsers Listing:


Available - Crosswalk - ionic browser add crosswalk
         Version 8.37.189.14 Published
         Version 9.38.208.10 Published
         Version 10.39.235.15 Published
         Version 11.40.277.7 Published
         Version 12.41.296.5 Published
(beta)   Version 13.42.319.6 Published
(canary) Version 14.42.334.0 Published

Available - Crosswalk-lite - ionic browser add crosswalk-lite
(canary) Version 10.39.234.1 Published
(canary) Version 10.39.236.1 Published

Available - Browser (default) - ionic browser revert android
Not Available Yet - GeckoView
```

At the current time, only Android is supported so just add for Android. As you can see on my result above, there are several Crosswalk version available. To add Crosswalk, issue this command,

```
$ ionic browser add crosswalk
```

By not specifying any version, Ionic will take the oldest version, which is **8.37.189.14** in my case. You can also specify a Crosswalk version,

```
$ ionic browser add crosswalk@12.41.296.5
```

To remove Crosswalk,

```
$ ionic browser revert android
```

or,

```
$ ionic browser rm crosswalk
```

The two commands do the same thing for Android.

To conclude, **always add Crosswalk browser for your Android apps**.

For more information about Crosswalk project, check out the following pages:

* [Ionic CLI Browser](http://ionicframework.com/docs/cli/browsers.html)
* [The Crosswalk Project](https://crosswalk-project.org/)
* [Intel Developer - Why use Crosswalk?](https://software.intel.com/en-us/xdk/docs/why-use-crosswalk-for-android-builds)



