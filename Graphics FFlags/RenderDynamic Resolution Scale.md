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
### How It Works

The value of `DFIntDebugDynamicRenderKiloPixels` determines the maximum number of kilopixels allowed for rendering. Lowering this value reduces the resolution, resulting in a more pixelated image.

#### Calculation Steps:

1. **Height × Width = Total Pixel Count**  
2. **Pixel Count ÷ 1000 = Kilopixel Value**  
3. **If the result includes a decimal, round it up to the nearest whole number.**

#### Example: 1080p Resolution

1. 1920 × 1080 = **2,073,600 pixels**  
2. 2,073,600 ÷ 1000 = **2073.6 kilopixels**  
3. Rounded up: **2074**
