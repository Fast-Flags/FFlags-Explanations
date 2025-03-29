### **FIntInterpolationAwareTargetTimeLerpHundredth (13)**  

#### What is `FIntInterpolationAwareTargetTimeLerpHundredth`?  

- This setting controls how aggressively the game interpolates frames.  
- Imagine an AI editing a single frame for a video while being aware of its surroundings.  
- The value ranges from **0 to 100**, with the original being **13%**.  
- **Higher values** lead to overcorrections, causing animations to freeze or teleport without smooth motion.  
- A setting of **100** works well with `DFIntMaxFrameBufferSize` set to **1-3**, as it improves AI awareness per keyframe.  

### Json:

```json
{
  "FIntInterpolationAwareTargetTimeLerpHundredth": "13"
}
```
