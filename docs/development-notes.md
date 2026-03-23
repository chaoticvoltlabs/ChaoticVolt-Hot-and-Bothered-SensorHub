# Development Notes

## Purpose of this document

This file captures the practical history and evolving role of Hot and Bothered SensorHub.

It is the right place for prototype history, tone-setting context, hardware lessons, and reminders about why the project exists in the first place.

## Origin story

This project started as a direct response to a real problem in daily life.

After a new heating and hot-water setup with a pellet boiler, solar collectors, PV, and the usual complexity that grows around such systems, failures could be inconvenient in a very specific way: you only discovered them after getting up and expecting warm water.

The installation was not right next to the living space. It was elsewhere on the property, in the former stable, so checking the system was not something you wanted to do casually every morning.

The original goal was therefore very simple:

- attach sensors
- publish useful values
- make the installation readable

## Why the name stayed

The playful name is not random. It comes directly from the original context.

The project grew out of wanting to know whether the hot-water system was actually hot — and whether anyone was about to be, quite literally, hot and bothered by the lack of it.

The name is memorable, and it still fits, even though the project now deserves a more mature presentation.

## Why the project became more serious

Once the SensorHub worked, it became obvious that it was not only useful at home.

An installer looking at the system immediately saw the value:

- remote visibility into thermal state
- quicker diagnosis
- fewer blind site visits
- better preparation before travel
- less guesswork for both technician and customer

That changed the nature of the project from:

- personal practical hack

into something closer to:

- a genuinely useful monitoring component

## Relationship to the display

The related display project is not an afterthought. It was part of the original reason for building the hub.

The display exists because a human-friendly, at-a-glance answer is sometimes more useful than a dashboard:

- is there hot water?
- is the boiler hot?
- is the system behaving normally?
- is a value missing or broken?

That is why the two projects fit together so naturally.

The split remains clean:

- **SensorHub** publishes the data
- **Display** presents the selected values

## Early field prototype

One early prototype ran for years in real service.

That matters, because it means the project was not just validated on a desk. It lived through actual use, actual startup cycles, and actual operational annoyance — which is exactly the kind of environment that reveals whether a monitoring node is genuinely useful.

This prototype also makes the relationship between the hub and the display especially concrete: the hub gathered the data, the display turned it into something a human could check at a glance.

## Olimex ESP32-EVB lesson

One of the more memorable lessons from that prototype generation was the **Olimex ESP32-EVB**.

It had a persistently awkward power-on reset behavior that never became fully satisfactory. The system could be made useful, and it ran for years, but the platform itself never felt truly clean on that point.

That is the kind of hardware lesson worth preserving in the documentation:

- not every long-running prototype is built on perfect hardware
- “works in practice” and “feels architecturally elegant” are not always the same thing
- some boards teach you as much through their annoying behavior as through their strengths

## Prototype reality

Like many useful projects, this one started in a quick and practical way.

That means the folder structure, naming, and some of the older repo tone may still reflect an earlier stage where the goal was simply to get something working fast.

That is not a flaw. It is normal.

The cleanup work in this repository is mostly about making the public face better match the actual value of the project.

## What should stay stable

Even if topic naming, integrations, or implementation details continue to evolve, the core identity of the project should remain stable:

it is a practical monitoring hub for temperature-heavy installations, with real value for local use, dashboards, and service workflows.

## Documentation rule

When in doubt:

- the origin story belongs here and in the README
- setup belongs in `UserGuide.md`
- MQTT structure belongs in `docs/mqtt-topics.md`
- system fit belongs in `docs/architecture.md`
- downstream consumer context belongs in `docs/integrations.md`
- raw historical scraps belong in `local_docs/legacy/`

That keeps the repo readable without losing the story that makes the project meaningful.
