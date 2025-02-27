# FFLAGS for Roblox

This document explains the purpose and usage of various FFLAGS categorized by functionality.

---

# PhysicSenderRate FFlag
```json
{
    "DFIntS2PhysicsSenderRate": "15"
}
```
> - #### Increasing this value results in more physical data being sent (e.g., jumping, walking, etc.), which can significantly improve synchronization with the server. This may reduce server-side client latency, making the player's movements appear more accurate to other users.
> - #### Lowering this value reduces the amount of physical data sent, which can be exploited for desynchronization. However, this does not provide a real advantage, as poor server-side synchronization can lead to issues such as enemies hitting you even when you are behind cover. (Not recommended)
- **Default Value:** 15
