### Control an infinite scroll properly.

The [infinite scroll](http://ionicframework.com/docs/api/directive/ionInfiniteScroll/) is usually applied to the ionic list and it is defined by,

```
<ion-infinite-scroll
    on-infinite="loadMore()"
    distance="1%">
</ion-infinite-scroll>
```

The `loadMore()` function will do basically two things,

* Job 1: Get data, process and update models accordingly to the view.
* Job 2: Broadcast the `scroll.infiniteScrollComplete` to tell the scroll to stop the loading UI.

If **job 2** goes missing, **the loading UI will never closed, it will show up forever**.

Another thing to point out, in the condition of having no more data to load, should we show up the loading spinner? Well, that depends on your apps' UX then. Since Ionic uses AngularJS, you can use [ng-if](https://docs.angularjs.org/api/ng/directive/ngIf) to check the condition to load.

```
<ion-infinite-scroll
    ng-if="shouldLoadMore()"
    on-infinite="loadMore()"
    distance="1%">
</ion-infinite-scroll>
```

**Playground**: http://play.ionic.io/app/b5493ff1700e



