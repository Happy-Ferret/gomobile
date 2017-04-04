# shiny

This is not the golang shiny driver ! That seems to have been subsumed by gomobile.
So moving right along...

GU is designed to power web based apps, but we want to use that approach on Desktop and Mobiles too - we are lazy geeks.
So, we use Webviews to host the GU Gopherjs code of ocurse.

Use gomobile bind call from native to golang
- You can call your golang library that you happen to also want to provide as an SDK to Native coders on any OS.
- just mak sure the methods and events conform to the limitation of the bind.

Use gomobile reverse to call from golang to native.
- can boot a webview
- can drive notification (from the app itself you can show a notification, so you dont need to use the network)
- You can show native widgets like dialogs and cal dialogs which tend to suck when done in the web browser

These currently work, but need modification and build up.

## Any OS lib
https://github.com/centrifugal
- an excellent example of how to write a golang library that works with bind.
- It also a great way to manage web socket communicates for chat etc too !


## OSX
https://github.com/murlokswarm/mac
- has everything there, but need to support a localhost golang server

https://github.com/jBugman/gomobile-test
- Because its Swift, it should also work on OSX


## Windows
https://github.com/murlokswarm/windows
- has everything there, but need to support a localhost golang server


## IOS
https://github.com/jBugman/gomobile-test
- uses Swift to host a golang web server on localhost


## Android
https://github.com/microo8/gowebview
- nice and easy

https://godoc.org/github.com/hyangah/mgodoc
- older and simpler

## Emulators
	# This seems to have some good stuff.
	#go get github.com/bitrise-steplib/steps-start-android-emulator
	
	

	
https://github.com/bitrise-tools/go-android/...
- go get github.com/bitrise-tools/go-android/...
- allows golang based controll over everything related to android sdk, ndk and avd (emulators).
- 
## Testing
Standard web tests canbe used since its just web.




## CI and Build
https://github.com/golang/build/tree/master/cmd/coordinator
- able to run builds using the golang teams approach.
