---
INFO: Rendering API
---

### Metal
> [!IMPORTANT]
> **MacOS Only**
```json
{
    "FFlagDebugGraphicsPreferD3D11": "false",
    "FFlagDebugGraphicsPreferD3D11FL10": "false",
    "FFlagDebugGraphicsPreferVulkan": "false",
    "FFlagDebugGraphicsPreferMetal": "true",
    "FFlagDebugGraphicsPreferOpenGL": "false"
}
```
### Vulkan
> [!CAUTION]
> **Visual bugs & crashes occur only in exclusive fullscreen.**
> **Fullscreen mode may cause crashes and does not support OBS Studio.**
```json
{
    "FFlagDebugGraphicsPreferD3D11": "false",
    "FFlagDebugGraphicsPreferD3D11FL10": "false",
    "FFlagDebugGraphicsPreferVulkan": "true",
    "FFlagDebugGraphicsPreferMetal": "false",
    "FFlagDebugGraphicsPreferOpenGL": "false"
}
```
### OpenGL
> [!IMPORTANT]
> - #### (More FPS on older devices do not support `future/unified` lighting.)
```json
{
    "FFlagDebugGraphicsPreferD3D11": "false",
    "FFlagDebugGraphicsPreferD3D11FL10": "false",
    "FFlagDebugGraphicsPreferVulkan": "false",
    "FFlagDebugGraphicsPreferMetal": "false",
    "FFlagDebugGraphicsPreferOpenGL": "true"
}
```
### Direct X 10
> [!IMPORTANT]
> - #### (More FPS on older devices do not support `future/unified` lighting.)
```json
{
    "FFlagDebugGraphicsPreferD3D11": "false",
    "FFlagDebugGraphicsPreferD3D11FL10": "True",
    "FFlagDebugGraphicsPreferVulkan": "false",
    "FFlagDebugGraphicsPreferMetal": "false",
    "FFlagDebugGraphicsPreferOpenGL": "false"
}
```
### Direct X 11
##### [DEFAULT API ENGINE WITH ALL FEATURES]
> [!IMPORTANT]
> - #### (More FPS on newest pc's)
```json
{
    "FFlagDebugGraphicsPreferD3D11": "True",
    "FFlagDebugGraphicsPreferD3D11FL10": "false",
    "FFlagDebugGraphicsPreferVulkan": "false",
    "FFlagDebugGraphicsPreferMetal": "false",
    "FFlagDebugGraphicsPreferOpenGL": "false"
}
```
