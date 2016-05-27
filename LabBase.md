# Lab 1: Create environment

You will learn:

* some basic elements such as a-scene, a-sky, a-sphere
* set color and positions

## Prerequisite

* [Firefox Developer Edition](https://www.mozilla.org/zh-TW/firefox/developer/)/Nightly or Chrome browser

## Start

Let's start from visiting demos from [https://aframe.io/](https://aframe.io/).

Once you are ready, you can use [https://jsfiddle.net/gasolin/gnp0maop/](https://jsfiddle.net/gasolin/gnp0maop/) to test functions of this Lab.

## Hello World

You can copy and paste
```
<a-scene>
  <a-sphere color="lightgreen"></a-sphere>
  <a-sky color="skyblue"></a-sky>
</a-scene>
```

In HTML body section. Hit `Run` button in jsfiddle to see how it changed.

![Imgur](http://i.imgur.com/EqGRuK8.png)

### Explain

You can reference element's document to find out what attribute it allow to set. Such as [a-scene](https://aframe.io/docs/core/scene.html), [a-sky](https://aframe.io/docs/primitives/a-sky.html), [a-sphere](https://aframe.io/docs/primitives/a-sphere.html)

## Change position and rotation

You can copy and paste
```
<a-scene>
  <a-sphere color="lightgreen" position="2 0 2"></a-sphere>
  <a-box color="red" position="2 2 0"></a-box>
  <a-sky color="skyblue"></a-sky>
</a-scene>
```

In HTML body section. Hit `Run` button in jsfiddle to see how it changed.

### Explain

We add another [a-box](https://aframe.io/docs/primitives/a-box.html) element with position.

The position is defined with `position = "x y z"` value.

![webgl xyz](http://obviam.net/wp-content/uploads/2011/01/Vertices.png)

We are also able to use [rotation](https://aframe.io/docs/components/rotation.html) attribute to change the angle of how the object is facing to the user. 

For example, `rotation = "10 20 30"` takes the roll (x), which rotation about the X-axis to 10 degree, pitch (y), rotation about the Y-axis to 20 degree, and yaw (z), rotation about the Z-axis to 30 degree. 

Combinding position and rotation could help you place the object anywhere as you expect.

## Your task

* Change colors and positions of existing elements,

* Check [Reference](https://aframe.io/docs/primitives/) and add `a-plane` behind the box and sphere, set it's height and width to 20.
