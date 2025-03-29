### **DFIntMaxAverageFrameDelayExceedFactor (3)**  

#### What is `DFIntMaxAverageFrameDelayExceedFactor`?  

- This setting controls how much **frame delay** can exceed the target frame time before the game corrects it.  
- **Frame time target:** Typically **16ms** for **60 FPS**.  
- **Average frame delay:** If the game calculates **48ms**, this setting determines when correction happens.  

#### **How It Works**  
- The exceed factor is a **multiplier** for the target frame time.  
- **Example:**  
  - If set to **2**, and the target frame time is **16ms**, then any delay **above 32ms** (16 × 2) will trigger a correction.  
  - Setting it to **0** may cause it to run indefinitely without correction.  
- Works well with `DFIntMaxFrameBufferSize` set to **1-3** for fine-tuned frame adjustments.  

### Json:  

```json
{
  "DFIntMaxAverageFrameDelayExceedFactor": "3"
}
```
