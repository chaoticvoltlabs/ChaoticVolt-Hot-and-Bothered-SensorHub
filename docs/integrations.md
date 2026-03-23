# Integrations

## Purpose of this document

This file explains how Hot and Bothered SensorHub fits into external systems and practical monitoring workflows.

The SensorHub is most useful when it acts as a readable, reliable source of installation data for downstream tools.

## Home Assistant

Home Assistant is a natural fit for this project.

Why it fits well:

- MQTT is already a common integration path
- sensor values can be visualized quickly
- automations and alerts are easy to build
- installation state becomes easy to inspect from phone or dashboard

## ThingsBoard

ThingsBoard is also a good fit when the goal is more monitoring-oriented or service-oriented.

Why it fits well:

- telemetry fits naturally
- dashboards can be structured around installation state
- multiple monitored systems become easier to compare
- service partners can inspect values before going on-site

This is particularly relevant for the installer/service use case that emerged after the original personal project.

## Related display project

The display project is one of the most direct integrations.

The relationship is intentionally simple:

- SensorHub publishes the useful data
- the display subscribes to and presents selected values

This matters because it preserves a clear split:

- the hub is the source of truth
- the display is the presentation layer
