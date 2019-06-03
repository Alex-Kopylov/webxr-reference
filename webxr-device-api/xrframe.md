# XRFrame

The **`XRFrame`** interface of the WebXR Device API provides all of the values needed to render a single frame of an AR/VR scene to the display 

An instance of this object is passed to each call of the callback provided to `XRSession.<a href="requestanimationframe">requestAnimationFrame()<a>`.

## Properties

<dl>
  <dt>session \{\{readonlyinline\}\}</dt>
  <dd>TBD</dd>
</dl>

## Methods

<dl>
  <dt>getPose()</dt>
  <dd>TBD</dd>
  <dt>getViewerPose()</dt>
  <dd>TBD</dd>
</dl>

## Examples

The following example show the use of `XRFrame`, which is always used inside a render loop. The loop is started by calling `requestAnimationFrame()` with a passed reference to a callback. The second parameter to that callback is a reference to an `XRFrame`.

```javascript
session.requestAnimationFrame(onFrame);

function onFrame(time, frame) {
  // 
}
```

## Specifications

[XRFrame Interface](https://immersive-web.github.io/webxr/#xrframe-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
