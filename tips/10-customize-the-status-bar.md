### Customize the status bar

To customize the status bar, you will have to add a Cordova plugin,

```
$ cordova plugin add cordova-plugin-statusbar

or

$ cordova plugin add org.apache.cordova.statusbar
```

Those two commands are the same, so don't worry if you see it different across many tutorials out there.

Basically, the Cordova plugin will make status bar being available through `window.StatusBar` object. If you spot on any Ionic project template, you will see the following part,

```js
if(window.StatusBar) {
    StatusBar.styleDefault();
}
```

The following methods are available through `window.StatusBar`:

```
* StatusBar.overlaysWebView()
* StatusBar.styleDefault()
* StatusBar.styleLightContent()
* StatusBar.styleBlackTranslucent()
* StatusBar.styleBlackOpaque()
* StatusBar.backgroundColorByName(namedColor)
* StatusBar.backgroundColorByHexString(hexColorString)
* StatusBar.hide()
* StatusBar.show()
```

For the `StatusBar.backgroundColorByName(namedColor)`, you need to provide a name `namedColor` that is pre-defined in the plugin, and they are:

```
"black": "#000000",
"darkGray": "#A9A9A9",
"lightGray": "#D3D3D3",
"white": "#FFFFFF",
"gray": "#808080",
"red": "#FF0000",
"green": "#00FF00",
"blue": "#0000FF",
"cyan": "#00FFFF",
"yellow": "#FFFF00",
"magenta": "#FF00FF",
"orange": "#FFA500",
"purple": "#800080",
"brown": "#A52A2A"
```

For the `StatusBar.backgroundColorByHexString(hexColorString)`, the string must be a valid color hex, eg., `#ff00ff`, `#3a3a3a`, `#40d5e7`... and must have `#` as prefix.

To determine if the status bar is visible on app, check it via `StatusBar.isVisible` property, which is a boolean.

For the plugin has pretty much methods for uses just to customizing color, there is a `ngCordova` plugin that wraps all of these, `$cordovaStatusbar`. Following methods are supported,

```
$cordovaStatusbar.overlaysWebView(true);

// styles: Default : 0, LightContent: 1, BlackTranslucent: 2, BlackOpaque: 3
$cordovaStatusbar.style(1);

// supported names: black, darkGray, lightGray, white, gray, red, green,
// blue, cyan, yellow, magenta, orange, purple, brown
$cordovaStatusbar.styleColor('black');

$cordovaStatusbar.styleHex('#000');

$cordovaStatusbar.hide();

$cordovaStatusbar.show();

var isVisible = $cordovaStatusbar.isVisible();
```

Visit these links for more information,

* [learn.ionic - Customizing the status bar](http://learn.ionicframework.com/formulas/customizing-the-status-bar/)
* [ngCordova - $cordovaStatusbar](http://ngcordova.com/docs/plugins/statusbar/)




