### Remove views from history

As you know, view history is managed through `$ionicHistory` service, and sometimes, there is a screen or page we don't want to store on navigation stack, and this is what you do,

```
$ionicHistory.nextViewOptions({
    disableAnimate: true,
    disableBack: true
});
```

Let say there are two screens, start from A and transition to B. We don't want to keep A in history stack, then put the above code in screen A controller when transitioning to screen B (for example, a button click...). This way, at screen B, users can't press *Back* button to return to screen A anymore.
