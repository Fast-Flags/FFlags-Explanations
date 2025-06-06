# Increasing Data Receive from RakNet

#### Data Receive from RakNet

```json
{
  "DFIntClientRecvFromRaknet": "255"
}
```

- **Maximum Value:** 255  
- **Minimum Value:** 0  
- **Default Value:** 0  
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
#### Using RakNet with MTU (Allows increasing the value above 1472):
```json
{
  "DFFlagRakNetMtuPing": "true"
}
```
