# XRWebGLLayer

The **`XRWebGLLayer`** interface of the WebXR API is an <a href="xrlayer">XRLayer</a> subtype that allows WebGL to provide the bitmaps to be rendered to a device. Only one layer can be used at a time. It is set by passing an instance of `XRWebGLLayer` or one of its siblings to <code><a href="xrsession">XRSession</a>.baseLayer</code> property.

## Constructor

<dl>
  <dt><a href="xrwebgllayer-constructor.md">XRWebGLLayer()</a></dt>
  <dd>Returns a new XRWebGLLayer object.</dd>
</dl>

## Properties

<dl>
  <dt>antialias \{\{readonlyinline\}\}</dt>
  <dd>Indicates whether the current layer supports antialiasing which helps smooth an image by reducing its jagged edges.</dd>

  <dt>context</dt>
  <dd>Returns an instance of <a href="xrwebglrenderingcontext">XRWebGLRenderingContext</a> which will be either a <a href="https://developer.mozilla.org/en-US/docs/Web/API/WebGLRenderingContext">WebGLRenderingContext</a> or a <a href="https://developer.mozilla.org/en-US/docs/Web/API/WebGL2RenderingContext">WebGL2RenderingContext</a> object.</dd>

  <dt>framebuffer \{\{readonlyinline\}\}</dt>
  <dd>TBD</dd>

  <dt>framebufferHeight \{\{readonlyinline\}\}</dt>
  <dd>TBD</dd>

  <dt>framebufferWidth \{\{readonlyinline\}\}</dt>
  <dd>TBD</dd>

  <dt>ignoreDepthValue \{\{readonlyinline\}\}</dt>
  <dd>TBD</dd>
</dl>

## Methods

<dl>
  <dt>getViewport()</dt>
  <dd>TBD</dd>

  <dt>getNativeFramebufferScaleFactor()</dt>
  <dd>For a specified <a href="xrsession">XRSession</a> object, returns the value that it's recommended WebGL frame buffer resolution must be multiplied by to yield it's native WebGL frame buffer resolution.</dd>

</dl>

## Examples

This example shows where in relation to session creation and starting the render loop that a layer should be set. The layer is set by setting `XRSession.baseLayer` to a new instance of `XRWebGLLayer`.

```javascript
// Do some Cottontail stuff.
let scene = new Scene();
scene.addNode(new CubeSea());

xrDevice.requestSession(sessionOptions)
.then(session => {
  // Use Cottontail's createWebGLContext() method.
  gl = createWebGLContext({
    // It needs an instance of XRDevice.
    compatibleXRDevice: session.device
  });
  // Use Cottontail's Renderer object.
  renderer = new Renderer(gl);
  scene.setRenderer(renderer);
  session.baseLayer = new XRWebGLLayer(session, gl);

  // Initialize the render loop.
})
```

## Specifications

[XRWebGLLayer Interface](https://www.w3.org/TR/webxr/#xrwebgllayer-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility).
