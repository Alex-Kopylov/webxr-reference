# XRInputSource

The **`XRInputSource`** interface of the of the WebXR API returns information about the Web AR/VR control device being used. The control device is platform-specific and defines a primary action. A primary action is a trigger, touchpad, button, spoken command, or hand gesture that when performed produces <a href="selectstart">selectstart</a>, <a href="selectend">selectend</a>, and <a href="select">select</a> events.

## Properties

<dl>
  <dt>gamepad</dt>
  <dd>TBD</dd>
  <dt>gripSpace</dt>
  <dd>TBD</dd>
  <dt>handedness</dt>
  <dd>One of <code>"left"</code>, <code>"right"</code>, or <code>""</code> (empty string).</dd>
  <dt>targetRayMode</dt>
  <dd>One of <code>"gazing"</code>, <code>"pointing"</code>, or <code>"tapping"</code></dd>
  <dt>targetRaySpace</dt>
  <dd>TBD</dd>
</dl>

## Methods

None.

## Examples

The following example taken from Immersive Web's [input tracking sample](https://github.com/immersive-web/webxr-samples/blob/master/input-tracking.html) uses `XRSession.getInputSources()` to get an array of `XRInputSource` objects. It then uses the first available input source to render representations of the input device in VR at appropriate locations. In the actual example, this function is called from within the `requestAnimationFrame()` callback. This insures the virtual positions of input devices are kept in sync with their physical counterparts.

```javascript
  // New example
```

# Specifications

[XRInputSource Interface](https://www.w3.org/TR/webxr/#xrinputsourceevent-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
