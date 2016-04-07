### Change Ionic serve address

By default, Ionic serve address will be set to **localhost**. Somehow, if you want to change to different address that bind to your network, you can use Ionic CLI to pick an address,

```
$ ionic address

Multiple addresses available.
Please select which address to use by entering its number from the list below:
 1) 192.168.100.3 (en0)
 2) localhost
Address Selection:  1
```

It seems like this command `ionic address` is not shown on Ionic CLI help list.
