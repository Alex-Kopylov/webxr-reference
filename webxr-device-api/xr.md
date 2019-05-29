# XR

The **`XR`** interface of the of the WebXR API provides methods for obtaining an XRSession object. Once a session is obtained, subsequent interactions with the hardware are done through it.

## Properties

None.

### Event Handlers

<dl>
  <dt>ondevicechange</dt>
  <dd>Called with a standard Event whenever device availability changes. </dd>
</dl>

## methods

<dl>
  <dt>supportsSession(options)</dt>
  <dd>Returns an empty promise that resolves if the requested session mode is available from the device. Valid options are
  <ul>
    <li><code>"inline"</code>: 
    <li><code>"immersive-vr"</code>: </li>
    <li><code>"immersive-ar"</code>: </li>
  </ul>
  </dd>
  <dt>requestSession(options)</dt>
  <dd>Returns a \{\{jsxref("Promise")\}\} that resolves with an <a href="xrsession">XRSession</a> object 
  Valid options are
  <ul>
    <li><code>"inline"</code>: 
    <li><code>"immersive-vr"</code>: </li>
    <li><code>"immersive-ar"</code>: </li>
  </ul></dd>
</dl>

## Examples

The following example uses the `ondevicechange` event to .

```javascript
navigator.xr.addEventListener('devicechange', () => {
  // Fill in
})
```

## Specifications

[XR Interface](https://www.w3.org/TR/webxr/#xr-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
