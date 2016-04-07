### Manage Ionic view lifecycle

When using AngularJS it is considered a good practice to load your data using the `$viewContentLoaded` event in controllers. When using Ionic SDK, this event is not usable, instead we have access to more specific events. The Ionic view cache comes with 8 new events, for instance `$ionicView.loaded` is triggered once per view being created and added to the DOM while the `$ionicView.enter` event will fire, whether it was the first load or a cached view.

Using the right event to load your data can improve the usability of the application. Indeed the less HTTP requests you send the better for the usability.

Here is the complete list of events that you can use with Ionic:

```
$scope.$on('$ionicView.loaded', function(){});
$scope.$on('$ionicView.enter', function(){});
$scope.$on('$ionicView.leave', function(){});
$scope.$on('$ionicView.beforeEnter', function(){});
$scope.$on('$ionicView.beforeLeave', function(){});
$scope.$on('$ionicView.afterEnter', function(){});
$scope.$on('$ionicView.afterLeave', function(){});
$scope.$on('$ionicView.unloaded', function(){});
```

Understanding Ionic view lifecycle will help us to handle events and actions more properly.