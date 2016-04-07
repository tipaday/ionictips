### Disable side menu swipe for a specific view

By default, all views based on side menu can be swiped to open the side menu. However, there might have one or several views that you don't want user to swipe out, so how to do it?

This little snippet will help,

```js
function disableSideMenuSwipe() {
    $scope.$on('$ionicView.enter', function() {
        $ionicSideMenuDelegate.canDragContent(false);
    });
    $scope.$on('$ionicView.leave', function() {
        $ionicSideMenuDelegate.canDragContent(true);
    });
}
```

So when a view is entered, `$ionicSideMenuDelegate` service will help to disable the drag ability (in other word, **swipe**) and re-enable when leaving. Without reset `canDragContent` to **true**, users can't swipe the side menu, so be aware of this option when use.