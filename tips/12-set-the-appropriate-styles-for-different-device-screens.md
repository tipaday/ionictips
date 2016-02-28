### Set the appropriate styles for different device screens

While developing mobile applications using Ionic framework, you will need to deal with different screen sizes across devices. Since things are just regular web user interface, so we will need to use `@media` for handling responsive.

While some properties like `min-width`, `max-width` work for browsers, **they don't work on mobile apps**.

```css
@media only screen and (min-width: 320px) and (max-width: 414px) {
    // define responsive styles here
}
```

Above example won't response to other styles, you won't see any change.

To handle this, we need to use the `device`-related properties, eg. `min-device-width`, `max-device-width`, which helps to detect the **physical dimension of the screen**.

```css
@media only screen and (max-device-width: 480px) {
    // define responsive styles here
}
```

Have fun :)

