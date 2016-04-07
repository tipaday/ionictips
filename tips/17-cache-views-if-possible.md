### Cache views if possible

By design, each Ionic screen or page is rendered as an `ion-view` directive. When there are a lot of pages, it apparently slows down during transition from pages to pages due to re-rendering. Lucklily, Ionic provides cache mechanism for views which is enabled by default with 10 views. When enabled it keeps views in the DOM cache with their scope, current state, and scroll position. When navigating you never lose your input or scroll position so you can go back in history without the fear of losing data.

> Views are cached to improve performance. When a view is navigated away from, its element is
left in the DOM, and its scope is disconnected from the $watch cycle. When navigating to a
view that is already cached, its scope is reconnected, and the existing element, which was
left in the DOM, becomes active again. This can be disabled, or the maximum number of cached
views changed in $ionicConfigProvider, in the view’s $state configuration, or
as an attribute on the view itself.

To config number of views to be cached,

```
$ionicConfigProvider.views.maxCache(10);
```

or can be set per platform,

```
$ionicConfigProvider.platform.android.views.maxCache(15);
$ionicConfigProvider.platform.ios.views.maxCache(15);
```


To disable cache for a specific view,

```
<ion-view cache-view="false">
```

or you can add `cache` option on `$stateProvider`,

```
$stateProvider.state('state', {
   cache: false,
   ...
});
```

View cache is a must and very important for improving performance on Ionic applications. Please be aware of this while developing your apps.
