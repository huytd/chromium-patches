# Chromium Patches

This repo contains selective patches for the Chromium project that I use for my personal browser. 

## How to use

Follow the following guides to clone the Chromium source code and build on macOS:

- https://chromium.googlesource.com/chromium/src/+/main/docs/mac_build_instructions.md
- https://gitlab.com/noencoding/OS-X-Chromium-with-proprietary-codecs/-/wikis/home (if you want to build with all proprietary codecs)

Current Chromium version:

```
git checkout tags/131.0.6748.1
```

You can copy the `patches` directory from this repository into your local Chromium's `src`. Then, apply the patch you want, for example:

```
git apply patches/allowManifestV2.patch
```

Then run the build:

```
autoninja -C out/Default chrome
```

## Patches

- [Allow ManifestV2 extensions](patches/allowManifestV2.patch) (so Ublock Origin can work)
