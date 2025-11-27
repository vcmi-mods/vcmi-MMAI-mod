# Overview

A [VCMI](https://github.com/vcmi/vcmi) mod for distributing pre-trained ML
models through the VCMI mod system.

## Mod release workflow

[This](https://github.com/vcmi-mods/mmai/actions/workflows/create-release.yml)
GHA workflow is used for mod releases. It will:

1. Create a release tagged `vcmi-VCMIVER-latest`, where `VCMIVER` is the
  compatibility version extracted from mod.json.
1. Upload a `vcmi-mod.zip` release asset for download by VCMI's mod manager.

If another release with this tag already exists, it is re-tagged as
`vcmi-VCMIVER-TIMESTAMP` so the new mod becomes downloadable via the old
URL.
