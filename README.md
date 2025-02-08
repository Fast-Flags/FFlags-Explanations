# Hey there This channel for explaining what does fflags do!
# DCD FFLAGS
---
### What does `FFlagSimEnableDCD16` do and what does it enable?

**DCD** stands for **Decomposition Detection**. It is a feature that helps detect and optimize complex objects, particularly in games, by analyzing their structure and simplifying them for better performance.

---

## How to enable Decomposition Detection (DCD)?

To enable DCD, use the following FFlag:

```json
{
  "FFlagSimEnableDCD16": "true"
}
```

When you enable this flag, it automatically activates the following fflags:
```json
{
  "DFIntSimCSG3DCDMaxNumConvexHulls": "1000",
  "FIntSimCSG3DCDRecomputeStrategy": "1",
  "DFIntSimCSG3DCDRecomputeTotalWaitMiliSec": "10000"
}
```
---
# MTU FFLAGS

## What is MTU?
- ### MTU (Maximum Transmission Unit) is the maximum size of a data packet that can be transmitted over a network without fragmentation.

- ### Simply put, it's the limit on how large a single chunk of data can be when sent over the internet or a local network. If a packet exceeds the MTU, it gets split into smaller pieces, which can slow down transmission.

- ### 👉 Roblox's default MTU size is **1396 bytes**.

## How to find the optimal MTU using a **ping test**?

### Windows:
1. Open the command prompt (**cmd**)
2. Enter the command:
   ```sh
   ping roblox.com -f -l [MTU size]
   ```
3. Start with **1472 bytes** and decrease the value by **10-12 bytes** until you find the largest value that does not cause fragmentation.
4. Once found, **add 28 bytes** to this value to get the **optimal MTU**.

### Example of setting MTU in Roblox:
```json
{
    "DFIntConnectionMTUSize": "MTU_HERE"
}
```

## How to increase MTU beyond 1472 without issues?
To allow higher MTU values without problems, add the following FFlag:
```json
{
    "DFFlagRakNetMtuPing": "True"
}
```
---
# Dynamic Resolution Scale
## What does dynamic Resolution Scale mean?
> - The Dynamic Resolution feature helps developers maintain their application’s frame rate while rendering at an optimal resolution. Dynamic Resolution automatically adjusts the resolution during heavy GPU work and increases image quality when possible.
### How to enable dynamic Resolution Scale in roblox?
```json
{
    "FFlagRenderDynamicResolutionScale11": "true"
}
```
> - ## Default value (false)
