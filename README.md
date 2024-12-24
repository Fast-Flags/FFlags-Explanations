# Hey there!

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
