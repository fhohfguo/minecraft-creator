---
author: JDHeaden
ms.author: v-jillheaden
title: Entity Documentation - minecraft:behavior.dig
ms.prod: gaming
---

# Entity Documentation - minecraft:behavior.dig

`minecraft:behavior.dig` [EXPERIMENTAL BEHAVIOR] activates the "DIGGING" actor flag during the specified duration. Currently only Warden can use the dig goal.

| Type| Name| Default Value| Description |
|:-----------:|:-----------:|:-----------:|:-----------:|


## Parameters

| Name| Default Value| Type| Description |
|:-----------:|:-----------:|:-----------:|:-----------:|
| allow_dig_when_named| false| Boolean| If true, this behavior can run when this entity is named. Otherwise not. |
| digs_in_daylight| false| Boolean| Indicates that the actor should start digging when it sees daylight |
| duration| 0.0| Decimal| Goal duration in seconds |
| idle_time| | Decimal| The minimum idle time in seconds between the last detected disturbance to the start of digging. |
| suspicion_is_disturbance| false| Boolean| If true, finding new suspicious locations count as disturbances that may delay the start of this goal. |
| vibration_is_disturbance| false| Boolean| If true, vibrations count as disturbances that may delay the start of this goal. |


## Vanilla entities examples

### warden

```json
"minecraft:behavior.dig": {
    "priority": 1,
    "duration": 5.5,
    "idle_time": 60.0,
    "vibration_is_disturbance": true,
    "suspicion_is_disturbance": true,
    "digs_in_daylight": false
},
```

## Vanilla entities using `dig`

- [warden](../../../../Source/VanillaBehaviorPack_Snippets/entities/warden.md)
