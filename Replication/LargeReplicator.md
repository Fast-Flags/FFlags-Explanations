# Enable Large Replicator:
```json
{
  "FFlagLargeReplicatorEnabled6": "True",
  "FFlagLargeReplicatorWrite5": "True",
  "FFlagLargeReplicatorRead5": "True",
  "FFlagLargeReplicatorSerializeRead2": "True",
  "FFlagLargeReplicatorSerializeWrite2": "True",

  "FFlagGlobalSettingsEngineModule3": "False",
  "DFFlagLargeReplicatorEngineModule": "True"
}
```
### Large replicator is a more advanced replicator
## Explanation:

### Main large replicator fflags:

```json
{
  "FFlagLargeReplicatorEnabled6": "True",
  "FFlagLargeReplicatorWrite5": "True",
  "FFlagLargeReplicatorRead5": "True"
}
```

#### Enables the Large Replicator system

---

### Caching Support:

```json
{
  "FFlagLargeReplicatorSerializeRead2": "True",
  "FFlagLargeReplicatorSerializeWrite2": "True"
}
```

#### Enables caching for the Large Replicator

---

### Engine Stability & Support Modules:

```json
{
  "FFlagGlobalSettingsEngineModule3": "False",
  "DFFlagLargeReplicatorEngineModule": "True"
}
```

#### Enables required engine modules and settings to prevent crashes.
#### Without these, enabling only the main flags may cause the client to crash.
