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
