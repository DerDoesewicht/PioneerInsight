# Pioneer Insight

> Discover resources, analyse production flow and understand your complete factory infrastructure directly on the Satisfactory map.

[Deutsch](README.de.md)

[![Pioneer Insight resource overview](screenshots/Insightresources.png)](screenshots/Insightresources.png)

Pioneer Insight turns the in-game map into a factory analysis and infrastructure overview. Find radar-discovered resources, inspect production supply and demand, understand transport networks, and follow complete train and freight routes without switching to an external tool.

Vanilla is supported. Ficsit Farming, Satisfactory Plus and compatible resource mods are optional integrations, not required dependencies.

## New in 1.0.0

- **Radar-aware resources.** Display legitimately discovered resource nodes and filter them by type, purity, usage and content source.
- **Production-flow insight.** Analyse source supply, productive demand, utilization, surplus, deficit, free capacity, consumers, buffers and final destinations.
- **Infrastructure overview.** Inspect production buildings, belts, pipes, stations, freight platforms, switches and connected rail networks on the map.
- **Train and freight analysis.** Browse locomotives, wagons, timetables, stops and cargo routes, then highlight the complete physical route of a selected train.
- **Multiplayer authority.** Dedicated servers provide authoritative resource, train and rail snapshots so client relevancy does not hide important data.
- **Large-network performance.** Train metadata loads first; the compressed full rail network follows in the background and remains cached across map reopenings.

## Four integrated map views

### Resources

Pioneer Insight adds a dedicated resource view beside the normal map filters. It displays only nodes discovered through the game's radar system and provides dynamic filters for every detected resource.

Filter by resource type, purity, free or occupied state, and content source. Modded resources are added automatically when compatible runtime data is available, including nodes stored in separate streamed worlds such as Ficsit Farming's resource levels.

### Flow

Hover over or select a resource node to inspect the connected production network. The analysis separates source supply from productive demand and shows the resulting balance, utilization and remaining capacity.

Consumers, buffers, transport buildings, overflow disposal and final destinations are listed separately. Additional diagnostics include machine counts, network segments, open branches, unused outputs, belt capacities and detected source bottlenecks.

Pioneer Insight analyses your existing factory. It does not change recipes, clock speeds or logistics.

### Infrastructure

Use the infrastructure view to understand how a large factory is connected. Production buildings, splitters, mergers, belts, pipes, stations, freight platforms, switches and rail vehicles can be inspected directly on the map.

Search and network filters help isolate the part of the factory you currently need instead of drawing every diagnostic layer at once.

### Trains and freight

The train view provides locomotive and wagon counts, resolved timetables, station sequences, cargo legs and route distances. Select a locomotive to inspect its complete timetable or highlight its physical path across the rail network.

Each route segment can report distance, traversed track segments and switch count. The map can also center on the selected locomotive.

## Features

- Dedicated Resources, Flow, Infrastructure and Trains pages inside the standard map.
- Dynamic filters for vanilla and compatible modded resources.
- Resource purity and free/occupied-state filters.
- Radar-respecting node visibility.
- Solid and fluid production-flow analysis.
- Supply, demand, utilization, surplus, deficit and available-capacity metrics.
- Separate consumers, buffers/transport, overflow/disposal and final-destination summaries.
- Belt and source-transport capacity diagnostics.
- Infrastructure search, selection and connected-network isolation.
- Full server rail-network rendering.
- Locomotive, wagon, timetable, station and freight-platform overview.
- Physical timetable-route highlighting over real rail splines.
- Server-authoritative multiplayer synchronization.
- English and German interface following the game language.

## Screenshots

### Resources

[![Resource filters and discovered nodes](screenshots/Insightresources.png)](screenshots/Insightresources.png)

### Production flow

[![Production supply and demand analysis](screenshots/Insightflow.png)](screenshots/Insightflow.png)

### Complete rail-network overview

[![Train and freight overview](screenshots/Insighttrains.png)](screenshots/Insighttrains.png)

### Physical train-route highlighting

[![Highlighted timetable route](screenshots/Trainsroutshighlight.png)](screenshots/Trainsroutshighlight.png)

Screenshots may include optional mod content and a developed save with a large rail network.

## Getting started

1. Install Pioneer Insight through Satisfactory Mod Manager.
2. For multiplayer, install the same version on the client and dedicated server.
3. Load your save and open the standard in-game map.
4. Select **Pioneer Insight**, then choose **Resources**, **Flow**, **Infrastructure** or **Trains**.

Resource visibility follows the game's radar discovery state. Pioneer Insight does not reveal undiscovered nodes.

## Compatibility

| Component | Support |
| --- | --- |
| Satisfactory | Game build `>=502094` |
| Satisfactory Mod Loader | `^3.12.0` required |
| Vanilla | Supported |
| Compatible resource mods | Runtime discovery |
| Ficsit Farming | Optional resource-node integration |
| Satisfactory Plus | Optional resource and factory integration |
| Multiplayer | Supported |
| Dedicated servers | Supported; same version recommended on server and clients |
| Interface | English and German |

Optional content appears only when its mod and required runtime data are available. Runtime discovery does not guarantee compatibility with every building or resource from every mod.

## Multiplayer and performance notes

On dedicated servers, Pioneer Insight requests authoritative resource, train and rail information. Train metadata is transferred first so locomotive and timetable information becomes available before the complete static rail network finishes loading.

The full rail geometry is compressed, transferred in the background and cached after arrival. Reopening the map or switching tabs does not rebuild unchanged rail geometry. Local client copies are suppressed after authoritative data arrives to prevent duplicate trains, timetables and rail segments.

The cache is reset when leaving or changing the gameplay world; it is not stored permanently between game sessions.

## Diagnostics and bug reports

Report reproducible bugs and feature requests through [GitHub Issues](https://github.com/DerDoesewicht/PioneerInsight/issues).

Please include:

- Game build, SML version and Pioneer Insight version.
- Single-player, multiplayer-client or dedicated-server context.
- Installed content and resource mods.
- Reproduction steps and screenshots.
- Relevant client/server log or crash report.
- A suitable diagnostic export when requested.

Available diagnostic console commands:

```text
PioneerInsight.Perf
PioneerInsight.ProbeRadar
PioneerInsight.ProbeInfrastructure
PioneerInsight.ProbeTrains
```

Discord: `derdoesewicht`

## Mod identity

- Public name: **Pioneer Insight**
- Technical mod reference: `PioneerCartographer`
- Current release: **1.0.0**

The technical mod reference intentionally remains `PioneerCartographer` for compatibility with existing installations, saves and multiplayer sessions.

This project is not affiliated with or endorsed by Coffee Stain Studios.
