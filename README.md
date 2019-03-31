# Bitmp4

[![Release](https://jitpack.io/v/blackdizel/Bitmp4.svg)](https://jitpack.io/#blackdizel/Bitmp4)

Based on https://github.com/dbof10/Bitmp4


Usage
---
In this example, we record a gif content and export to a video file.
For more information, please check out the [sample app](https://github.com/dbof10/Bitmp4/tree/master/app).

Basic setup:

~~~ java
 MP4Encoder encoder = new MP4Encoder();
 encoder.setFrameRate(20); //frames per second
 encoder.setOutputFilePath(someFilePath); //output video file path. something like blablabla/test.mp4
 encoder.setOutputSize(1280, 720); //frame width and height
 encoder.startEncode();
 for (Bitmap item : bitmaps) //where bitmaps is your bitmap collection
   encoder.addFrame(item);
 encoder.notifyLastFrameAdded();
~~~

API:

~~~ kotlin
 startExport()
 
 stopExport()
 
 addFrame(bitmap) //called intervally
 
 setEncodeFinishListener()
 
 setEncodeFrameListener()
~~~

Download
--------
While we are working on Bintray support, Bitmp4 is available via Jitpack.

##### Gradle:
```groovy
repositories {
    // ...
    maven { url "https://jitpack.io" }
}

implementation 'com.github.dbof10:Bitmp4:0.1'
```

Apps using Bitmp4
---
[Live Message](https://play.google.com/store/apps/details?id=com.ctech.livemessage)

[BC Stop Motion animation](https://play.google.com/store/apps/details?id=org.byters.bcphotoanimations)

License
-------

    Copyright 2018 Ctech Inc

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
