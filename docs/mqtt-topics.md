# MQTT Topics

## Purpose of this document

This file is the canonical place for topic naming, payload expectations, and practical MQTT usage notes for Hot and Bothered SensorHub.

The exact topic layout may evolve, but the guiding idea should stay stable:

- topics should be predictable
- sensor names should be understandable
- retained state should be used deliberately
- downstream integrations should not have to guess

## Topic design goals

The MQTT structure should make the hub useful for:

- dashboards
- Home Assistant
- ThingsBoard
- service-monitoring tools
- the related display project
- simple custom scripts

That means topics should be:

- readable
- stable
- easy to map to installation concepts
- not overloaded with historical naming accidents

## Recommended topic shape

A clear pattern is preferable to ad-hoc topic sprawl.

Suggested style:

```text
hotandbothered/<device-id>/<category>/<name>
```

Examples:

```text
hotandbothered/sensorhub-01/temperature/boiler
hotandbothered/sensorhub-01/temperature/buffer_top
hotandbothered/sensorhub-01/temperature/return_line
hotandbothered/sensorhub-01/temperature/utility_room
hotandbothered/sensorhub-01/status/online
hotandbothered/sensorhub-01/status/uptime
hotandbothered/sensorhub-01/relay/pump
hotandbothered/sensorhub-01/system/ip
```

If a shorter or older structure already exists in the code, document both, but aim for a stable canonical form in public docs.
