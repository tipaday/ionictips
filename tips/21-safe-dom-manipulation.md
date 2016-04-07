### Safe DOM Manipulation

Because Ionic is built with AngularJS, therefore, we can use the provided **JQlite** for DOM manipulation. However, you should do DOM processing only when DOM is ready, otherwise, it will not work or something unexpected happens.

```js
ionic.DomUtil.ready(function () {
    // ready
    var title = angular.element(document.getElementById('title'));
})
```

This way, views will be safe from unexpected behavior.