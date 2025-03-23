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
