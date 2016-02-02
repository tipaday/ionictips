### Create a correct iOS project configuration

There is one bug in Ionic CLI is that, while creating project via command-line, even if you specify the flag **--appname** for app name and **--id** for app package id, it won't do anything on iOS project config.

What I mean is this,

```
$ ionic start awesome-app blank --appname "Awesome App" --id "com.tipaday.awesomeapp"
```

After project creation, checkout the **platforms/ios** directory,

* The project name should refect what app name is, and not **HelloCordova**.
* Widget name and id in **HelloCordava** are not updated.

```
<widget id="com.ionicframework.starter" version="0.0.1" xmlns="http://www.w3.org/ns/widgets" xmlns:cdv="http://cordova.apache.org/ns/1.0">
    ...
    <name>HelloCordova</name>
    <description>
        An Ionic Framework and Cordova project.
    </description>
    <author email="you@example.com" href="http://example.com.com/">
      Your Name Here
    </author>
```

**How to fix it**

After creating new projects, just remove the platform if it is already added.

```
$ ionic platform rm ios
```

Open the **config.xml** at root directory and update correct information, eg. **name**, **id**, **author**, **description**...

then issue the platform command again,

```
$ ionic platform add ios
```

You will see the newly-added iOS project has been updated with the correct name and correct config information.

**NOTE: this bug of Ionic CLI happens with v1.7.14 and below.**

**For Android projects, the package id is updated correctly automatically on AndroidManifest.xml and res/values.xml; so there is no need to worry about it.**



