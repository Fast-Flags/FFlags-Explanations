# FFLAGS for Roblox

This document explains the purpose and usage of various FFLAGS categorized by functionality.

---
# MTU (Maximum Transmission Unit) FFLAGS

#### What is MTU?

-  **MTU** is the maximum size of a data packet that can be transmitted over a network without fragmentation.
-  If a packet exceeds the MTU, it gets split into smaller pieces, potentially slowing down transmission.
-  **Roblox's default MTU size is 1396 bytes.**

### How to Find the Optimal MTU?

1. **Open Command Prompt** (cmd).
2. **Run the following command:**
   ```sh
   ping roblox.com -f -l [MTU size]
   ```
3. **Start with 1472 bytes** and decrease the value by **10-12 bytes** until you find the largest value that does not cause fragmentation.
4. **Add 28 bytes** to this value to get the **optimal MTU**.

#### Setting MTU in Roblox:

```json
{
    "DFIntConnectionMTUSize": "MTU_HERE"
}
```

#### Increasing MTU Beyond 1472 Without Issues:

```json
{
  "DFFlagRakNetMtuPing": "true"
}
```

---

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

# Increasing Data Receive from RakNet

#### Adjusting RakNet Data Reception

```json
{
  "DFIntClientRecvFromRaknet": "255"
}
```

- **Maximum Value:** 255  
- **Minimum Value:** 0  
- **Default Value:** 0  

---

# Optimizing Clicks & Reducing Input Latency

#### What is `FIntCLI20390_2`?

- #### **CLI** stands for **Client**. This flag adjusts mouse input queues or debounce time (measured in milliseconds between clicks before the next input is registered).
-  Default is **16ms** to prevent accidental double clicks.
-  Useful for spam-clicking scenarios (e.g., [Blade Ball](https://www.roblox.com/games/13772394625/Blade-Ball)).
-  Example: Setting **10000ms (10 seconds)** delays input for that time.

### Example Configuration

```json
{
  "FIntCLI20390_2": "0"
}
```

---

# RakNet Enable Polling

### Enabling Polling in RakNet

```json
{
  "DFFlagRakNetEnablePoll": "true"
}
```

### Purpose

- Enables polling in **Roblox's RakNet** networking library.
- Allows frequent checks for incoming/outgoing packets.

### Benefits

- **Improves networking responsiveness** and reduces latency.
- **May increase CPU usage** due to continuous polling.

---

# Memory Utility (Affects Memory Usage in Roblox)

### Configurable Memory Utility Flags

#### **`DFIntMemoryUtilityCurveBaseHundrethsPercent`**
-  Defines base percentage for memory utility curve (hundredths of a percent).
-  Higher values (e.g., **10000 or 100%**) assume full memory utilization.

#### **`DFIntMemoryUtilityCurveNumSegments`**
-  Determines the number of segments in memory utility calculations.
-  More segments increase accuracy but may slightly impact performance.

#### **`DFIntMemoryUtilityCurveTotalMemoryReserve`**
-  Specifies total memory reserve for utility calculations.
-  **0 means no extra memory is reserved**.

### Example Json:
```json
{
  "DFIntMemoryUtilityCurveBaseHundrethsPercent": "10000",
  "DFIntMemoryUtilityCurveNumSegments": "100",
  "DFIntMemoryUtilityCurveTotalMemoryReserve": "0"
}
```
---

# PhysicSenderRate FFlag
```json
{
    "DFIntS2PhysicsSenderRate": "15"
}
```
-  Increasing this value results in more physical data being transmitted (e.g., jumping, walking, etc.), significantly improving synchronization with the server. This can reduce server-side client latency, making player movements appear more precise to other users.  
-  Lowering this value decreases the amount of physical data sent, which can be exploited to create desynchronization. However, this does not offer any real advantage, as poor server-side synchronization can cause issues like enemies hitting you even when you are behind cover. *(Not recommended)*  

- **Default Value:** 15  
## Some players refer to this FFlag as "Fast Dash" in [**The Strongest Battlegrounds**](https://www.roblox.com/games/10449761463/The-Strongest-Battlegrounds), but this is incorrect. This is not a "**faster dash**" or any kind of exploit. Instead, this FFlag enhances synchronization with the server.  
---
# Dynamic Render KiloPixels(Related to dynamic res scale):
```json
{
"DFIntDebugDynamicRenderKiloPixels":"2"
}
```
### How does its work:

- A lower value of `DFIntDebugDynamicRenderKiloPixels` decreases the number of kilopixels, resulting in a lower resolution and a more pixelated image.
---
