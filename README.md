<div align="center">

<!-- LOGO -->

# Parallel Worlds

**Temporary mining dimensions, fresh on a schedule — NeoForge 1.21.1**

</div>

---

Parallel Worlds adds isolated **exploration dimensions** for mining and looting so your main world never gets strip-mined. Pick a destination through the portal, dig everything up, and come back — the dimension resets on schedule either on restart or after some time of inactivity.

Dimensions are cloned directly from your server's world generator, so modded biomes, structures, and even dimensions work out of the box.
This you can use to provide new Worlds for adventures, without mixing and destroying your main worlds.

---

## Getting in

**Portal (default)** — Build a frame out of the configured block (default: glass), light it with the configured item (default: flint and steel), and step through. Sneak + right-click with the cycle item to scroll through dimension targets; the portal color changes to show where you'll land.

**Commands (optional)** — `/pw tp` and `/pw return` are disabled by default but can be turned on in config. Useful for servers that don't want the portal requirement.

---

## Highly configurable features

**Offered Dimensions** - You're in control for which dimensions can have a parallel dimension.

**Seed Rotation** - Choose whether or not to have the seed changed on reset and when. Choose reset to be daily, weekly, or monthly and exactly on what hour and minute the reset should occur.

**Automatic Returns** - Players actively exploring a parallel dimension have their return positions saved in case dimensions are being reset or they lose connection to the server.

**Persistence** - Your choice on how the parallel dimension is handled. Shall it be kept until server restarts? Or maybe until the seed rotation? How about dynamically as the world is explored? 

**Retention Period** - Want the old worlds scrapped or a configurable amount of them saved, so an admin could enter them again should the need arise.

**Map Mod Compatibility** - Dimension maps that are cached from popular mods like **Xaero's Minimap**, **Xaero's World Map**, **JourneyMap**, and even **Distant Horizons** are automatically wiped on each client that reconnects to your server. No old tiles or LOD files are saved. Feature can be disabled with `modCompatCleanupEnabled = false` in each client-side config.

**Chunk pre-generation** — Optionally pre-generate a radius of chunks around spawn when a new dimension is created. The generator is TPS-aware: full speed above 19.5 TPS, throttled below 19.0, paused below 18.0. This avoids lag spikes during normal play but will consume some extra CPU in the background — tune the radius and chunk budget per tick to match your hardware.

**Async noise computation** — Noise and heightmap calculations can be offloaded to worker threads so chunk generation doesn't block the main thread. Disabled by default; enable with `asyncChunkGenerationEnabled = true`. The worker count defaults to half your available CPU cores and is configurable.

---
