# Lab 2: Create 360 image

You will learn:
* take 360 image with Streeview app
* a-asset

What you will make:

* [360 Image with WebVR](http://gasolin.github.io/webvrdemo/streetview.html)

## Prerequisite

* Android or iOS device
* Please make sure you understand [first Lab](LabBase) before following this Lab.

## Import Library

According to the [getting start guide](https://aframe.io/docs/guide/getting-started.html)

To create a brand new WebVR web page, we can drop a `script` tag straight into our HTML to include A-Frame in normal web page:

```
<script src="https://aframe.io/releases/0.2.0/aframe.min.js"></script>
```

Or, [fork this project](https://github.com/gasolin/webvrdemo) to start. Click up right `fork` button on `https://github.com/gasolin/webvrdemo` github page, it will fork a clone to your own repository.

## Take 360 image with Streeview app

First, search and download [streetview app](https://play.google.com/store/apps/details?id=com.google.android.street) from Play Store or App Store.

![Imgur](http://i.imgur.com/qDOZvK9l.png)

Open the app, tap `+` button then tap `camera` button to start take a 360 image.

![Imgur](http://i.imgur.com/TPJ1tQul.png)

Center the white circle on the orange dot, then trace the other dot by moving the phone.

Tap the green dot once the images surround you. It will take sometime to prepare a 360 image.

![Imgur](http://i.imgur.com/gPBpFJUl.png)

Check [slide](http://www.slideshare.net/proyectoste/how-to-create-360-images-with-google-street-view-app) page 20 to export the photo for later use.

## Show image with A-Frame

You can copy and paste

```
<a-scene>
  <a-assets>
    <img id="office" src="PANO_20160523_135032_0.jpg">
  </a-assets>
  <a-sky src="#office" rotation="0 -130 0"></a-sky>
</a-scene>
```

In the body section, or refer to [streetview.html](https://github.com/gasolin/webvrdemo/blob/gh-pages/streetview.html) where you forked.

### Explain

To be rendered correctly, the images applied here should use [equirectangular projection](https://en.wikipedia.org/wiki/Equirectangular_projection).

[a-sky](https://aframe.io/docs/primitives/a-sky.html) provide a large sphere to render our 360 image on it. Change the `radius` attribute will influence the distance between you and the 360 image.

Define images, audio, video in [a-assets](https://aframe.io/docs/core/asset-management-system.html) could help A-Frame better manage memory resources.

## Your task

* Replace your image in the `img` tag, then reload the page to see how it looks like.

Previous Lab's answer: https://jsfiddle.net/gasolin/cq7ffozd/
