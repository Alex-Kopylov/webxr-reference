# XRRenderState

The **`XRRenderState`** interface of the WebXR API provides information about the user's environment.

## Properties

<dl>
  <dt>baseLayer \{\{readonlyinline\}\}</dt>
  <dd>The <code><a href="xrlayer">XRLayer</a></code> instance that is the source of bitmap images and a description of how the image is to be rendered in the device.</dd>

  <dt>depthFar \{\{readonlyinline\}\}</dt>
  <dd>The distance in meters of the far clip plane from the viewer.</dd>

  <dt>depthNear \{\{readonlyinline\}\}</dt>
  <dd>The distance in meters of the near clip plane from the viewer.</dd>

  <dt>inlineVerticalFiledOfView \{\{readonlyinline\}\}</dt>
  <dd>Defines the angle of the field of view in radians used when computing projection matrices for an `inline` `XRSession` objects. This option must be `null` for immersive sessions.</dd>
</dl>

### Events

None.

## Methods

None.

## Examples

TBD

## Specifications

[XRRenderState Interface](https://immersive-web.github.io/webxr/#xrrenderstate-interface)

## Browser Compatibility

See [Browser Compatibility](compatibility) for general information.
