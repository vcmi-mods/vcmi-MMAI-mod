# MMAI

Pre-trained models for VCMI's combat AI powered by machine learning.

<img src="screenshots/screenshot-01.png" alt="components" height="300px">

## Mod release workflow

[This](https://github.com/vcmi-mods/mmai/actions/workflows/create-release.yml)
GHA workflow should be used for mod releases. It will:

1. Parse [models/sources.json](mmai/models/sources.json), download the
  models (provided by
  [vcmi-gym](https://github.com/smanolloff/vcmi-gym)) and update
  [config/settings.json](mmai/config/settings.json)
  
1. Create a release tagged `vcmi-VCMIVER-latest`, where `VCMIVER` is the
  compatibility version extracted from mod.json.
1. Upload a `mod.zip` release asset to be downloaded by VCMI's mod manager.

If another release with this tag already exists, it is re-tagged as
`vcmi-VCMIVER-TIMESTAMP` so the new mod becomes downloadable via the old
URL.

#### Example

A new VCMI version `1.8.0` is released and mod compatibility must be updated accordingly:
1. Update `mmai/mod.json` (directly in main branch)
1. Run the [workflow](https://github.com/vcmi-mods/mmai/actions/workflows/create-release.yml).

Release `vcmi-1.8-latest` will appear shortly.
