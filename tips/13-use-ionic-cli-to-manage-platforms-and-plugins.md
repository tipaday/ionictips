### Use Ionic CLI to manage platforms and plugins

Ionic framework comes with Ionic CLI tool to help developers managing platforms and plugins. A very common mistake that many people face is that, they just copy projects from somewhere else, and then use them without configuring via Ionic CLI. As a result, their projects will not work.

To build project for a specific platform, like iOS or Android, this command must be done,

```
$ ionic platform add ios

$ ionic platform add android
```

When grabbing a project somewhere to the local machine, you need to install necessary Cordova plugins before running it,

```
$ ionic state restore
```

All of these platform and plugins information is stored in `package.json` like this,

```
"cordovaPlugins": [
    "cordova-plugin-whitelist@1.0.0",
    "cordova-plugin-inappbrowser@1.0.1",
    "cordova-plugin-splashscreen@2.1.0"
],
"cordovaPlatforms": [
    "android",
    "ios"
]
```

This way, all Ionic projects are synced across developers' machines.