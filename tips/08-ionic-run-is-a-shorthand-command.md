### ionic run is a shorthand command

Everytime you want to build your code and make it run, these steps are taken

```
// to emulate
$ ionic build && ionic emulate

// to run on device
$ ionic build && ionic run
```

Forget about it, there is one single command that can help running those steps.

```
$ ionic run
```

What it does is to run a build first, and then detect if there is any connected device to execute, or else, it will try to run on pre-configured emulator.

That's it and make it run!
