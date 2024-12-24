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
---
### Let's start with what does mtu mean?
## Mtu = maximum transmission unit  (Packets)

(Roblox default mtu size is 1396)
### Whats optimal mtu for me?
> [!TIP]
> **Identify the Current MTU**
> - **Windows**: Open Command Prompt and type `netsh interface ipv4 show subinterfaces`.
> - **Linux**: Use `ifconfig` or `ip link show` to find the current MTU of your network interface.
> [!TIP]
> **Determine the Optimal MTU**
> - **Ping Test**: Use the `ping` command with the `-f` flag (to avoid fragmentation) and the `-l` (or `-s` on Linux) flag to set the packet size.
> - **Example for Windows**:
>   ```bash
>   ping roblox.com -f -l 1472
>   ```
> - **Example for Linux**:
>   ```bash
>   ping -s 1472 -M do roblox.com
>   ```
> - Start with a packet size of 1472 bytes, then reduce by 10-12 bytes if needed until you find the largest size that doesn't fragment. Add 28 bytes to this number to get the optimal MTU.

```json
{
    "DFIntConnectionMTUSize": "MTU_HERE"
}
```
---
