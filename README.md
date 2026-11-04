# MiCyte Datasets

The public datum feeds of the MiCyte network, each with a history of its own.

| File | Schema | What it holds |
|---|---|---|
| [`almanac/taxonomy.json`](almanac/taxonomy.json) | `micyte.almanac.taxonomy.v1` | The Almanac's biological classification: 4,696 taxa, one node per row with its level and its parent, and the profiles a taxon carries. |
| [`registry.json`](registry.json) | `micyte.registry.v1` | The msn contact-card registry: 182 public cards, each with its entity kind and status. |

Each file states its own `schema`, `source` and `note`. Read those before relying on a field.

## Where they come from

Both files are derived from the network's datum store (MOS) by the MiCyte publishers on the host
that runs micyte.com, which serves them at <https://micyte.com/assets/almanac/taxonomy.json> and
<https://micyte.com/assets/registry.json>.

**State on 2026-11-04.** This repository was seeded with the exact bytes micyte.com served that day:

| File | sha256 |
|---|---|
| `almanac/taxonomy.json` | `aca8f32ad38d9f2d0253ee5aab6d2e594716170946170480cfee008c0dfcc0d8` |
| `registry.json` | `f69ff152b78d44b22021374395517435ebb32a86b092fa1d06602c7191339a0c` |

The publishers do not write here yet. Until they do ([#1](https://github.com/MiCyte/Datasets/issues/1)),
the copy micyte.com serves is the current one, and these files can fall behind it.

## License

The data in this repository is licensed under the Creative Commons Attribution-ShareAlike 4.0
International license (CC BY-SA 4.0): see `LICENSE`. You may copy, adapt and build on it, for
any purpose, if you credit MiCyte and release what you derive from it under the same license.
The share-alike condition covers adaptations of the data itself; the MiCyte code is licensed
separately (AGPL-3.0, in its own repositories).

## Contributing

A wrong taxon or card is corrected at its source, not in these files: the next publish would
overwrite a pull request that edits a feed. Open an issue naming the row (its `id`) and what is
wrong. Every commit needs a sign-off (`git commit -s`), the
[Developer Certificate of Origin](https://developercertificate.org).
