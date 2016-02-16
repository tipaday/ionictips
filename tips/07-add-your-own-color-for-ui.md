### Add your own color for UI

Ionic framework provides a pretty cool list of color for common use. However, if you want to have your own color for UI without do too much work, just override one of base colors defined in `scss/ionic.app.scss`

First make sure to setup SASS for project,

```
$ ionic setup sass
```

Open the SASS file, you will see something like this commented,

```
$light:                           #fff !default;
$stable:                          #f8f8f8 !default;
$positive:                        #387ef5 !default;
$calm:                            #11c1f3 !default;
$balanced:                        #33cd5f !default;
$energized:                       #ffc900 !default;
$assertive:                       #ef473a !default;
$royal:                           #886aea !default;
$dark:                            #444 !default;
```

Those are pre-defined colors in Ionic, so we can pick one color to override all correspondent UI components. For example, if we want all **dark**-colored components to be in **#2c3e50**, just add right below the comment paragraph,

```
$dark : #2c3e50 !default;
```

Run `gulp` to rebuild the CSS from SCSS, and now all **dark**-colored components will reflect change with the new color, eg. `bar-dark`, `button-dark`, `toggle-dark` ...


