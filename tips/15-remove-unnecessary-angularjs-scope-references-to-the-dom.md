### Remove unnecessary AngularJS scope references to the DOM

By default, AngularJS just adds some scope references to the DOM, which are used to tools to debug or log tracking, such as Batarang. Those are unnecessary for production applications since it impacts on Ionic app performance. So just remove it when releasing applications.

```
angular.module('yourModule').config(function($compileProvider) {
    if (/* test if in production */) {
        $compileProvider.debugInfoEnabled(false);
    }
});
```

Have fun :)