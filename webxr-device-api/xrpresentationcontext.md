# XRPresentationContext

The `**XRPresentationContext**` interface of the WebXR API is a wrapper object for the \{\{domxref("HTMLCanvasElement")\}\} object on which AR or VR content will be drawn. To retrieve an instance of this object, call `getContext()` on a canvas object with the value `'xrpresent'`.

## Properties

<dl>
  <dt>canvas \{\{readonlyinline\}\}</dt>
  <dd>A reference to an \{\{domxref("HTMLCanvasElement")\}\} on which AR or VR content will be drawn.</dd>
</dl>

## Methods

None.

## Examples

The following example uses an instance of `XRPresentationContext` to query an XRDevice object for session support. Though this code tries to convey something of the full context where the interface is used, getting and using it comes down to this:

```javascript
  // need code
```

# Specifications

[XRPresentationContext Interface](https://immersive-web.github.io/webxr/#xrpresentationcontext-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
