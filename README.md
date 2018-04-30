# ExoPlayerTest
Project to test how ExoPlayer works. It includes a plug-in that counts the times the video has been paused and resumed.
This plug-in also shows on screen a message when the video is paused,
and when it is resumed (and for how many seconds the video was paused).
In addition, it makes an API call the first time the video loads, when the first frame is played, 
and another one when the video finishes.
## Getting Started
First of all, if you want to get the whole project, it is as easy as cloning the whole project.
In case you just want the plug-in, you'll have to take just the exoplayer-plugin module,
then add it as a dependency on your main module gradle file.
```
dependencies {
  ...
  implementation project(':exoplayer-plugin')
}
```
After adding the dependency, you will have to call the plugin from the activity where you are using ExoPlayer, 
and add it as a listener. 
```
yourExoPlayerObject.addListener(new PluginListener(view, context)
```
Where view will be the view where you want the messages to show up, and context will be the own activity.
And so it should work correctly.
## Built With
* [ExoPlayer](https://github.com/google/ExoPlayer) - Google's media player for Android
