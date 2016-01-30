### Test Services from Console

This is a pretty popular trick among Angular developers.

From console screen, you can get an instance of the service you want to test.

```
var injector = angular.element(document).injector();
var service = injector.get('SERVICE_NAME')
```

Replace **SERVICE_NAME** with the name of service you want to test. Also, for quick work on console, you can make it in one line.

```
> angular.element(document).injector().get('SERVICE_NAME')
```

For a more precise selection, you should pick up the element that is directed by **ng-app** attribute.

```
> angular.element('*[ng-app]').injector().get('SERVICE_NAME');
```

Somehow, it might become handy under app development for many Ionic developers, I guess :)
