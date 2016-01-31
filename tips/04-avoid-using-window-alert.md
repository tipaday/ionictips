### Avoid using window.alert()

So you might ask,

> Why should I not use window.alert()?

Because it blocks UI and prevent any wait-to-be-done scripts to proper execution. It is also one of the common cause known while developing, that is, any UI click will trigger `window.alert()` [twice in a row](https://github.com/driftyco/ionic/issues/4345#issuecomment-139026496).

**Sometimes, window.alert() is good while developing apps, if not using it, what are the other options?**

Okay, you can use [$window.alert()](https://docs.angularjs.org/api/ng/service/$window).

Or even better, use the [$ionicPopup](http://ionicframework.com/docs/api/service/$ionicPopup/).

About this, it's all up to you, but that is a recommendation from my experiences.

