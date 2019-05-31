# XR

The **`XR`** interface of the of the WebXR API provides methods for obtaining an <a href="xrsession">XRSession</a> object. Once a session is obtained, subsequent interactions with the hardware are done through it.

## Properties

None.

### Event Handlers

<dl>
  <dt>ondevicechange</dt>
  <dd>Called whenever device availability changes. </dd>
</dl>

## methods

<dl>
  <dt>supportsSession(options)</dt>
  <dd>Returns an empty promise that resolves if the requested session mode is available from the device. Valid options are
  <ul>
    <li><code>"inline"</code>: Indicates that the sessions's output will be shown as an element in the HTML document. Content for an <code>"inline"</code> session may be displayed in mono or stereo and may allow viewer tracking.</li>
    <li><code>"immersive-vr"</code>: Indicates that the session's output will have exclusive access to the device and that content will not be integrated with the user's environment. </li>
    <li><code>"immersive-ar"</code>: Indicates that the session's output will have exclusive access to the device and that content will be integrated with the user's environment.</li>
  </ul>
  </dd>
  <dt>requestSession(options)</dt>
  <dd>Returns a \{\{jsxref("Promise")\}\} that resolves with an <a href="xrsession">XRSession</a> object 
  Valid options are
  <ul>
    <li><code>"inline"</code>: Indicates that the sessions's output will be shown as an element in the HTML document. Content for an <code>"inline"</code> session may be displayed in mono or stereo and may allow viewer tracking.</li>
    <li><code>"immersive-vr"</code>: Indicates that the session's output will have exclusive access to the device and that content will not be integrated with the user's environment. </li>
    <li><code>"immersive-ar"</code>: Indicates that the session's output will have exclusive access to the device and that content will be integrated with the user's environment.</li>
  </ul>
  </dd>
</dl>

## Examples

The following example uses the `ondevicechange` event to discover when a new device is available, then calls `requestDevice()` to retrieve it.

```javascript
navigator.xr.addEventListener('devicechange', () => {
  navigator.xr.requestDevice()
  .then(device => {
    // device is of type XRDevice. Use it to get an XRSession object.
  });
});
```

## Specifications

[XR Interface](https://www.w3.org/TR/webxr/#xr-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
