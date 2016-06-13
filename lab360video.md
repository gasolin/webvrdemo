# Lab 4: Create 360 image

You will learn:
* take 360 image with Streeview app
* a-videosphere

What you will make:

## Prerequisite

* A 360 camera, this lab need extra device to shot the 360 video
* Please make sure you understand the [first Lab](LabBase.md) before following this Lab.

## Take 360 video with 360 Camera

Either Ricoh Theta S, LG 360 CAM or other similar devices can do the job.

## Show video with A-Frame

You can copy and paste

```html
<a-scene>
  <a-assets>
    <video id="train" src="train.mp4">
  </a-assets>
  <a-videosphere src="#train" radius="100"></a-videosphere>
</a-scene>
```

In the body section. We do not provide the demo video at this moment because of the size.

### Explain

[a-videosphere](https://aframe.io/docs/primitives/a-videosphere.html) provide a large sphere to render our 360 video on it. Change the `radius` attribute will influence the distance between you and the 360 video.

Define images, audio, video in [a-assets](https://aframe.io/docs/core/asset-management-system.html) could help A-Frame better manage memory resources.

## Your task

* 
