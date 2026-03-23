# Overview

## Summary

Hot and Bothered SensorHub is an ESP32-based temperature monitoring and relay-control hub for heating, hot-water, and technical installation monitoring.

It began as a practical answer to a very practical question: **is there going to be hot water in the morning, or are you walking into a cold shower?**

A number of DS18B20 sensors were attached to a heating and hot-water installation, the readings were published to MQTT, and the system quickly became useful for more than just personal reassurance. The same data can also support remote monitoring, diagnostics, and service preparation.

## Role in the wider setup

The SensorHub is the **data-producing side** of the system.

Its responsibilities include:

- reading distributed temperature sensors
- publishing measurements to MQTT
- exposing local status and configuration
- supporting relay or installation-side control where needed
- acting as the upstream source for dashboards, automation, and the related display project

This repository is not the display client itself. It is the part that gathers, structures, and publishes the data that other tools and interfaces can use.

## Why it matters

The project turned a complicated heating installation into something measurable and visible.

That is useful in several different contexts:

- **daily use** — quickly see if the system is behaving normally
- **local display use** — drive an at-a-glance display in the bathroom or utility area
- **remote monitoring** — publish data into Home Assistant, ThingsBoard, or other MQTT-based tooling
- **service work** — inspect key values before going on-site

## What this repository does

This repository is intended to contain the SensorHub firmware and related documentation for:

- DS18B20 sensor acquisition
- MQTT publishing
- local web-facing configuration or status
- relay or control participation where appropriate
- practical integration with external systems

## What this repository is not

This repository is not primarily:

- the display client
- a generic smart-home marketing project
- an abstract “ultimate IoT platform”
- only a personal one-off hack, even if that is how it started

The best way to think about it is this:

it is a **practical monitoring component** with a real origin story and real use beyond that first origin story.

## Related project

This SensorHub has a clear sister-project relationship with the display client.

The relationship is simple:

- **SensorHub** gathers and publishes the data
- **Display** turns that data into immediate visibility

That pairing is part of what makes the project especially compelling, but the SensorHub also works perfectly well on its own through MQTT and dashboards.
