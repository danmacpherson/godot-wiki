# Requirements

*  Scons (you can get it from macports, you should be able to run "scons" on a terminal when installed)
*  Xcode with the iOS SDK and the command line tools.

# Compiling

Open a Terminal, go to the root dir of the engine source code and type:
```
$ scons bin/godot.iphone
```
for a debug build, or:
```
$ scons bin/godot_opt.iphone target=release
```
for a release build (check platform/iphone/detect.py for the compiler flags used for each configuration)

Alternatively, you can run

```
$ scons bin/godot.isim
```
for a Simulator executable.

# Run

To run on a device or simulator, follow these instructions: [Exporting for iOS](https://github.com/okamstudio/godot/wiki/export_ios)  
Replace or add your executable to the Xcode project, and change the "executable name" property on Info.plist accordingly if you use an alternative build.



