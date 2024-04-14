# IC10-programs
Compilation of IC10 programs for Stationeers.

## Battery Stats

Displays basic battery stats. Change the device type hash to the batteries in use.
Might update later to support mixed battery types.

## Solar Tracking

Tracks solar panels to Verticle and Horizontal positioning of the sun.

Setup:
- Link items to d# ports as listed.
- The daylight sensor and solar panels should all have the data connector facing north (0 degrees).

## Fire Door

Set of double doors that function as an airlock without airvents. Won't stop air
leaks or mixing, but function as emergency doors that won't explosively decompress.

## Airlock

Cycles doors and pulls a vauume to keep interior and exterior gasses from mixing.

Setup:
- Link items to d# ports as listed

Might have fixed values for inside and outside pressure, or sensors to read to auto equalize from tanks.

## Pressureize Room

Fills a room with gas. It is much faster if the Active vent is on the outside of the room set to inward.
