### Improve performance with one-time binding

[Introduced in Angular 1.3](https://docs.angularjs.org/guide/expression#one-time-binding), one-time binding saves developers from a lot of performance troubles with data binding,

> An expression that starts with `::` is considered a one-time expression. One-time expressions will stop recalculating once they are stable, which happens after the first digest if the expression result is a non-undefined value.

After populated, the data will be rendered once and removed from the watch list, which means it won't be re-rendered again if there is any change. And it is a good point to implement in Ionic applications in screens that we only want to display data and having no concern over data change.

```
<p>{{::firstname}}</p>
<p>{{::lastname}}</p>

<ul>
    <li ng-repeat="friend in ::friends_list">{{friend.name}}</li>
</ul>
```

On the bottom line, please review throughout the whole Ionic application to find out, which pages only need to render data once, which pages do not.
