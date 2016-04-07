### Monitor device internet connectivity

To check for Internet connection, we will need to use [**cordova-plugin-network-information**](http://ngcordova.com/docs/plugins/network/), to install,

```
$ cordova plugin add cordova-plugin-network-information
```

To monitor, we will bind the event provided by the plugin to the `$rootScope`,

```
// listen for Online event
$rootScope.$on('$cordovaNetwork:online', function(event, networkState){
    // do something when device is ONLINE
});

// listen for Offline event
$rootScope.$on('$cordovaNetwork:offline', function(event, networkState){
    // do something when device is OFFLINE
});
```

To check for current network status, call `$cordovaNetwork.isOnline()` and `$cordovaNetwork.isOffline()` to know.

Additionally, to get the type of network connection, use `getNetwork()`, it will return a **Connection** object with one of the following value.

Connection Type | Description
--------------- | -----------
Connection.UNKNOWN | Unknown connection
Connection.ETHERNET | Ethernet connection
Connection.WIFI | WiFi connection
Connection.CELL_2G | Cell 2G connection
Connection.CELL_3G | Cell 3G connection
Connection.CELL_4G | Cell 4G connection
Connection.CELL | Cell generic connection
Connection.NONE | No network connection



