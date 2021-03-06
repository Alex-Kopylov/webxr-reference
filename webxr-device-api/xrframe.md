# XRFrame

**Note**: Based on early versions of the spec, this interface was called `XRPresentationFrame` in early implementations.

The **`XRFrame`** interface of the WebXR Device API provides all of the values needed to render a single frame of an AR/VR scene to the display represented by the <a href="xrdevice.md">XRDevice</a> interface. An instance of this object is passed to each call of the callback provided to `XRSession.<a href="requestanimationframe">requestAnimationFrame()<a>`.

## Properties

<dl>
  <dt>views</dt>
  <dd>Returns an array of <a href="xrview">XRView</a> objects. A view is a display or portion of a display used by an AR/VR device to present imagery to the viewer.</dd>
</dl>

## Methods

<dl>
  <dt>getDevicePose()</dt>
  <dd>Takes an <a href="xrcoordinatesystem">XRCoordinateSystem</a> object and returns the state of the the position and orientation of viewer. Unless the value of `XRFrameOfReference` is `"headMode"`, this function is not guaranteed to return a value.</dd>
  <dt>getInputPose()</dt>
  <dd>Takes a reference to <a href="xrinputsource">XRInputSource</a> and <a href="xrframeofreference">XRFrameOfReference</a> objects and returns the position and orientation of the specified `XRInputSource`.
</dl>

## Examples

The following example show the use of `XRFrame`, which is always used inside a render loop. The loop is started by calling `requestAnimationFrame()` with a passed reference to a callback. The second parameter to that callback is a reference to an `XRFrame`.

```javascript
session.requestAnimationFrame(onFrame);

function onFrame(time, frame) {
  // frame is of type XRFrame.
  let pose = frame.getDevicePose(xrFrameOfRef);
  if (pose) {
    for (let view of frame.views) {
      scene.draw(view.projectionMatrix, pose.getViewMatrix(view))
    }
  }
  frame.session.requestAnimationFrame(onFrame);
}
```

## Specifications

[XRFrame Interface](https://immersive-web.github.io/webxr/spec/latest/#xrpresentationframe-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
