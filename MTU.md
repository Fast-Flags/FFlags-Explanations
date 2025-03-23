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
