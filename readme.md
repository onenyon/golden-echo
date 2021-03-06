# Carolina

![Carolina, 2015](https://mir-s3-cdn-cf.behance.net/project_modules/disp/bc94f328587235.55c8ec9517524.gif)

## Synopsis

Take a road trip through Kimbra’s song Carolina. View a landscape composed of vocals, guitars, bass, mellotrons, and more using your smartphone! Tap to change the perspective, pinch-to-zoom in and out and take in all the layers of this uplifting song with a colorful and abstract environment. Each item on the trip represents a specific sound in the song. Together they create a road to Carolina.

This is a port of an application made by [jonobr1](http://jonobr1.com/) specifically for Kimbra’s album release, The Golden Echo. For more by Kimbra check out her website: http://kimbramusic.com

Also, check out the project on [Android Experiments](http://androidexperiments.com/experiment/carolina)

## Technical

While Carolina is a native Android Application, it’s actually a packaged website! The project was developed on Google Chrome and then deployed using the [Mobile Chrome Apps](https://github.com/MobileChromeApps/mobile-chrome-apps) Command Line Interface, [CCA](https://github.com/MobileChromeApps/mobile-chrome-apps/blob/master/docs/Installation.md#install-the-cca-command-line-tool). This made development smooth because I was able to develop and debug using [Chrome Developer Tools](https://developer.chrome.com/devtools), then deploy as an Android Application for final proofing.

The contents of the app itself is divided into two different parts. There is the introduction and the music visualization. The introduction serves two purposes. First, I wanted a way to introduce the interactions and concept. Then as an added benefit I needed a loading screen while all the geometry was created and the song was loaded. Despite all the files being local on the device it takes about 10 seconds to load everything. The perfect amount of time for an introduction! The introduction is made up of a [Two.js](http://jonobr1.github.io/two.js) scene, a two-dimensional drawing api that I author.

The music visualization uses [Three.js](http://threejs.org), a popular three-dimensional drawing api for the web. I place a camera in the world and make it move along a [spline](https://github.com/mrdoob/three.js/blob/master/src/extras/curves/SplineCurve3.js). I then create a number of different types of shapes for the various instruments in the track. As the song plays each shape has specific triggers. When one of these triggers occurs the shape is placed in the impending field of view of the camera. As the camera moves the shape flies by as if we were in a car or a train passing through a landscape.

This repository is the source code to create that project.

### **this is an [android experiment](http://androidexperiments.com)**

The MIT License (MIT)

Copyright (c) 2015 jonobr1

Permission is hereby granted, free of charge, to any person obtaining a copy
of this source code and associated documentation files, but not assets and other
resources such as audio, video, or imagery files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

