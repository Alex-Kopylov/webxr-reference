# XRFrame

The **`XRFrame`** interface of the WebXR Device API represents a snapshot of the state of all tracked objects for an XRSession. Tracked objects include the headset, controllers, and possibly hands, if they're being exposed as input sources. An instance of this object is passed to each call of the callback provided to `XRSession.<a href="requestanimationframe">requestAnimationFrame()<a>`.

## Properties

<dl>
  <dt>session \{\{readonlyinline\}\}</dt>
  <dd>A reference to the <code><a href="xrsession">XRSession</a></code> that produced the frame.</dd>
</dl>

## Methods

<dl>
  <dt>getPose()</dt>
  <dd>Returns an <code><a href="xrpose">XRPose</a></code> instance which describes a position and orientation in space relative to an <code><a href="xrspace">XRSpace</a></code>.</dd>

  <dt>getViewerPose(xrReferenceSpace)</dt>
  <dd>Returns an <code><a href="xrpose">XRViewerPose</a></code> relative to the supplied <code><a href="xrreferencespace">XRReferenceSpace</a></code> describing the state of a viewer of the XR scene. The viewer may represent a tracked piece of hardware, or the observed position of the user's head relative to the hardware.</code></dd>
</dl>

## Examples

The following example shows the use of `XRFrame`, which is 

```javascript

```

## Specifications

[XRFrame Interface](https://immersive-web.github.io/webxr/#xrframe-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
