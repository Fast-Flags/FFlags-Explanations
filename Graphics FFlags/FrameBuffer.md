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
