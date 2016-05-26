# Lab 3: Create panorama image

You will learn:
* take panorama image with Cardboard Camera app
* a-curvedimage

What you will make:

* [360 degree panorama with WebVR](http://gasolin.github.io/webvrdemo/cardboardcam)
* [Partial panorama with WebVR](http://gasolin.github.io/webvrdemo/)

## Prerequisite

* Android or iOS device
* Please make sure you understand [Lab 1](LabBase) before following this Lab.

[fork this project](https://github.com/gasolin/webvrdemo) to start. Click up right `fork` button on `https://github.com/gasolin/webvrdemo` github page, it will fork a clone to your own repository.

## Take panorama image with Cardboard Camera app

Search and download [Cardboard Camera app](https://play.google.com/store/apps/details?id=com.google.vr.cyclops) from Play Store or App Store.

![Imgur](http://i.imgur.com/8zSj5qYl.png)

Tap `camera` button to start take the photo.

![Imgur](http://i.imgur.com/qHO5T6Fl.png)

Follow the direction of the red arrow. Turn around in steady speed to take a 360 panorama.

Though you can stop any time when you feel its sufficient.

![Imgur](http://i.imgur.com/QbU8YGZl.png)

It takes some time to prepare the panorama photo. Once its done, you can view and share it via your photo app (on Android). On iOS you might need install `Google Photos`.

## Show image with A-Frame

You can copy and paste

```
<a-scene>
  <a-curvedimage src="2016-05-23-14.51.12.jpg"
    height="140" radius="100" theta-length="360"
    rotation="0 0 0"></a-curvedimage>
  <a-sky color="darkgrey"></a-sky>
</a-scene>
```

In the body section, or refer to [cardboardcam.html](https://github.com/gasolin/webvrdemo/blob/gh-pages/cardboardcam.html) where you forked.

### Explain

[a-curvedimage](https://aframe.io/docs/primitives/a-curvedimage.html) is inherit from a-cylinder. It means the images will be bend around the user.
The `radius` is set to the default value of [a-sky](https://aframe.io/docs/primitives/a-sky.html#Attributes), so you will get the similar view distance. For 360 panorama, we set `theta-length="360"` to denote the image is surround the user for 360 degree. For partial panorama, you can set the value to what suit for your image.

## Your task

1. Replace your image in the `src` attribute of the `a-curvedimage` tag, then reload the page to see how it looks like.

2. Reference the [previous Lab](Lab360Image), use `a-assets` and #id to define the image resource in `a-asset` tag.
