### Enable Native Scrolling for Android

There is a really huge performance gain when applying **Native Scrolling** for Android, like when interacting with *Pull-to-Refresh*, *List View* ...

From Ionic 1.2+, Native Scrolling is enable by default.
For previous Ionic version, you can enable it by configuring the `$ionicConfigProvider`.

```
$ionicConfigProvider.platform.android.scrolling.jsScrolling(false);
```

Sometimes, there are pages that you don't want to apply Native Scrolling, and to disable it, switch `overflow-scroll` option to `false` on `ion-content` directive of the page,

```
<ion-content overflow-scroll="false">
```

One important to note that **Native Scrolling is not working when running on `collection-repeat`**,

> One important caveat is that because of how collection-repeat works, it requires rapidly shifting the scroll content, hijacking the scroll behavior, and recreating the scrollbar. That’s pretty much JS scrolling, so we set it so that collection-repeat will force an ion-content to use JS scrolling.

Quote from [Ionic Blog, Native Scrolling in Ionic: A Tale in Rhyme](http://blog.ionic.io/native-scrolling-in-ionic-a-tale-in-rhyme/)