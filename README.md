--- 
# FFLAGS for Roblox

This document explains the purpose and usage of various FFLAGS.

---

## DCD FFLAGS

### What does `FFlagSimEnableDCD16` do?

**DCD** stands for **Decomposition Detection**.

Enabling this flag automatically activates the following settings:

```json
{
  "DFIntSimCSG3DCDMaxNumConvexHulls": "1000",
  "FIntSimCSG3DCDRecomputeStrategy": "1",
  "DFIntSimCSG3DCDRecomputeTotalWaitMiliSec": "10000"
}
```

### How to enable DCD?

To enable DCD, set the following flag:

```json
{
  "FFlagSimEnableDCD16": "true"
}
```

---

## MTU FFLAGS

### What is MTU?

- **MTU (Maximum Transmission Unit)** is the maximum size of a data packet that can be transmitted over a network without fragmentation.
- Simply put, it limits the size of a single data chunk sent over the internet or a local network. If a packet exceeds the MTU, it gets split into smaller pieces, potentially slowing down transmission.
- **Roblox's default MTU size is 1396 bytes.**

### How to find the optimal MTU using a **ping test**?

1. **Open the command prompt** (cmd).
2. **Run the following command:**
   ```sh
   ping roblox.com -f -l [MTU size]
   ```
3. **Start with 1472 bytes** and decrease the value by **10-12 bytes** until you find the largest value that does not cause fragmentation.
4. **Add 28 bytes** to this value to get the **optimal MTU**.

### Example of setting MTU in Roblox:

```json
{
    "DFIntConnectionMTUSize": "MTU_HERE"
}
```

### How to increase MTU beyond 1472 without issues?

To allow higher MTU values without problems, add the following FFlag:

```json
{
  "DFFlagRakNetMtuPing": "True"
}
```

---

## Dynamic Resolution Scale

### What is Dynamic Resolution Scale?

Dynamic Resolution Scale helps developers maintain the application's frame rate by automatically adjusting the resolution during heavy GPU load and enhancing image quality when possible.

### How to enable Dynamic Resolution Scale in Roblox?

```json
{
  "FFlagRenderDynamicResolutionScale12": "true"
}
```

---

## Increasing Data Receive from RakNet

### How to increase the data received from RakNet?

Use the following FFlag to adjust:

```json
{
  "DFIntClientRecvFromRaknet": "255"
}
```

- **Maximum value:** 255  
- **Minimum value:** 0  
- **Default value:** 0

---

## Optimizing Clicks and Reducing Input Latency

### What does `FIntCLI20390_2` do?

#### CLI is short for client; this flag in particular allows you to adjust mouse input queues or its debounce time as Id like to interpret it, measured in milliseconds between clicks before the next input is registered. Its defaulted to 16ms for stability to prevent accidental double clicking. This only seems useful if you use your mouse in spam based scenarios such as blade ball for example. As mentioned before its measured in milliseconds so experimenting with higher values say 10000ms (10 seconds) will delay your next input by that specified amount of time 

#### Example Configuration:

- **Default value:** 16
- Example:

```json
{
  "FIntCLI20390_2": "0"
}
```

---
