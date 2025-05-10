# SurfaceAppearance and MaterialService in Roblox

Official documentation links:
- [SurfaceAppearance](https://create.roblox.com/docs/art/modeling/surface-appearance)
- [MaterialService](https://create.roblox.com/docs/reference/engine/classes/MaterialService)

## PBR and ACR

**PBR** (Physically-Based Rendering) is responsible for rendering various **SurfaceAppearance** textures as part of **MaterialService**, which is used to manage materials in games.

The following flags enable **ACR** (no official documentation available) over PBR, which results in objects and terrain not loading their assigned textures.

Compared to `SkipMips`, these flags do **not** degrade the quality of GUIs and similar assets, which can be more ideal for the user.

### Flags:
```json
{
  "FFlagTextureUseACR3": "True",
  "FIntTextureUseACRHundredthPercent": "10000"
}
```
# RESULT:
## BEFORE:
![Image](https://media.discordapp.net/attachments/1285949000595275847/1370818571353194497/image.png?ex=6820e1c7&is=681f9047&hm=a7dcf7299b3aacd31354842ece634084b992a5784fd9f371c4186ba63e3439dc&=&width=2091&height=1041)
## AFTER:
![Image](https://media.discordapp.net/attachments/1285949000595275847/1370818928934391849/image.png?ex=6820e21d&is=681f909d&hm=b942ef53bde6acca3b9f2e06d5255895946eddc6014e98162f68ff5c542f8b42&=&width=2094&height=1041)

> [!CAUTION]
> **Only removes textures from default Roblox materials, not custom SurfaceAppearance textures**
