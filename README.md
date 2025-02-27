# FFLAGS for Roblox

This document explains the purpose and usage of various FFLAGS categorized by functionality.

---

# PhysicSenderRate FFlag
```json
{
    "DFIntS2PhysicsSenderRate": "15"
}
```
- #### Increasing this value results in more physical data being transmitted (e.g., jumping, walking, etc.), significantly improving synchronization with the server. This can reduce server-side client latency, making player movements appear more precise to other users.  
- #### Lowering this value decreases the amount of physical data sent, which can be exploited to create desynchronization. However, this does not offer any real advantage, as poor server-side synchronization can cause issues like enemies hitting you even when you are behind cover. *(Not recommended)*  

- **Default Value:** 15  
## Some players refer to this FFlag as "Fast Dash" in [**The Strongest Battlegrounds**](https://www.roblox.com/games/10449761463/The-Strongest-Battlegrounds), but this is incorrect. This is not a "**faster dash**" or any kind of exploit. Instead, this FFlag enhances synchronization with the server.  

For example, if your usual ping is **50-70 ms**, enabling this setting improves synchronization, making **anti-shove** behave as if your connection had a server-side latency of **35-45 ms**.  
---
