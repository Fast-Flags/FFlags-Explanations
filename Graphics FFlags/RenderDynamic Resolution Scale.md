# Dynamic Resolution Scaling FFLAGS

#### What is Dynamic Resolution Scaling?

#### This feature helps maintain the game's frame rate by automatically adjusting resolution based on GPU load.

### Enable Dynamic Resolution Scaling:

```json
{
  "FFlagRenderDynamicResolutionScale12": "true"
}
```
### This feature is now enabled by default.
 -  To disable it make the value to `false`
---
# Dynamic Render KiloPixels
## (Related to dynamic resolution scaling):
```json
{
"DFIntDebugDynamicRenderKiloPixels":"2"
}
```
### How does its work:

- A lower value of `DFIntDebugDynamicRenderKiloPixels` decreases the number of kilopixels, resulting in a lower resolution and a more pixelated image.
