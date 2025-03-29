### **DFIntMaxFrameBufferSize (10)**  

#### What is `DFIntMaxFrameBufferSize`?  

- This setting determines how many frames are stored in the animation buffer before being rendered.  
- **Roblox sets it high** to prevent jitters, as an overly full buffer can cause uneven playback.  
- If too many frames are stored, the client struggles to sync them properly, leading to jerky animations.  

#### **Optimal Values**  
- **4-10** → Ideal for most games, ensuring smooth animation playback.  
- **1-3** → Harder to smooth out but reduces rendering load, often causing visible stuttering.  
- Lower values are generally preferred for responsiveness, but they require additional flags to compensate for stutter.  

### Json:
```json
{
  "DFIntMaxFrameBufferSize": "10"
}
```
---
### **How to make value `1` work without animation lags?**

To optimize the use of `DFIntMaxFrameBufferSize` set to **1** without experiencing animation lags, you can adjust the following settings:

```json
{
    "DFIntMaxFrameBufferSize": "1",
    "FIntInterpolationAwareTargetTimeLerpHundredth": "100",
    "DFIntMaxAverageFrameDelayExceedFactor": "0"
}
```

#### **Explanation of Settings:**

- **`DFIntMaxFrameBufferSize: 1`**  
  - Limits the number of frames stored in the buffer, reducing the rendering load but potentially causing jitter if not balanced correctly. Using this value effectively requires adjusting other flags to avoid animation stuttering.

- **`FIntInterpolationAwareTargetTimeLerpHundredth: 100`**  
  - Increases the game's interpolation aggressiveness, allowing smoother transitions between frames. At `100`, it helps prevent animation freeze or teleportation by improving the AI's awareness per keyframe, making it easier to smooth out the rendered output.

- **`DFIntMaxAverageFrameDelayExceedFactor: 0`**  
  - This ensures that there is no limit on how much the average frame delay can exceed the target frame time. By setting it to **0**, you allow frames to be corrected indefinitely, giving more flexibility for performance without triggering immediate corrections on slight delays.

### **Related Links:**

- [Frame Delay Exceed Factor](https://github.com/Fast-Flags/FFlags-Explanations/blob/main/Graphics%20FFlags/Frame%20Delay%20Exceed%20Factor.md)  
- [Interpolation Aware Time](https://github.com/Fast-Flags/FFlags-Explanations/blob/main/Interpolation%20FFlags/Interpolation%20Aware%20Time.md)  

By using these settings, you should be able to work with **`DFIntMaxFrameBufferSize: 1`** while minimizing animation lags, as the interpolation and delay factors are optimized for smoother performance.
