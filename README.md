# Waydex county packs

Landmark packs for **Waydex**, a free Android car-journey tracker with a game-style radar minimap. Each English ceremonial county has its own pack, built from OpenStreetMap. The app offers a county's pack after a drive into it, or from Settings → County packs. Every pack is listed in the latest release.

## What's in a pack

Each `<COUNTY>.pack.db.gz` is a gzip-compressed SQLite database. Waydex opens it as a read-only Room database, schema version 5. It holds:

- **landmarks** to drive through: roundabouts and mini-roundabouts, bridges and tunnels of 100 m or more (or named), roadside viewpoints, services, tolls and ferries. Each landmark is in the pack of the county its centre lies in;
- **hazards** the app never scores, but notes after a trip with a safety tip: level crossings and fords;
- **road junctions**, with the direction of each road. These separate a turn at a junction from a bend in the road;
- the **public through-roads**, as a cell mask, where new roads earn discovery XP;
- **towns and villages** for trip names, **railway lines** for spotting train journeys, and **car parks** for ignoring parking manoeuvres;
- the **county outline**.

`catalog.json` lists every pack with its download size, SHA-256 checksum, OpenStreetMap data date and number of landmarks. The app checks the checksum before installing a pack.

West Yorkshire and the East Riding of Yorkshire ship inside the app, so they aren't here.

## Licence and attribution

- The packs are derived from OpenStreetMap: **© OpenStreetMap contributors**. They're available under the [Open Database License 1.0](https://opendatacommons.org/licenses/odbl/1-0/) (ODbL). If you use them, you must say they're from OpenStreetMap, and anything you build from them must stay under the ODbL.
- The county outlines contain OS data © Crown copyright and database right 2025, used under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). They come from OS Boundary-Line.
- The OpenStreetMap data comes from [Geofabrik](https://download.geofabrik.de/europe/united-kingdom/england.html)'s county extracts, and each pack records its own data date.

See [LICENSE.md](LICENSE.md).

## Privacy

Downloading a pack is an ordinary request to GitHub. GitHub sees your IP address and which county you asked for. The packs contain no personal data, and Waydex sends nothing else.
