# conversion-compatibility

This repository is **fully automated** and managed by GitHub Actions workflows. Its contents should not be edited manually.

## Purpose

This repository acts as a single source of truth for the file format conversion pairs supported by the transmute.sh conversion service. By decoupling this data from the main source code, we avoid any impact on existing CI/CD pipelines or development workflows.

## How it works

- `supported_conversions.json` is published to this repository automatically on commit to main in [transmute-app/transmute](https://github.com/transmute-app/transmute).
- The file is served directly from this repository via GitHub's raw content delivery, making it accessible at a stable, predictable URL.
- No manual intervention is required — all updates are handled by automation.

## Contents

Each entry in the JSON file has the following shape:

```json
{
    "converter_name": "FFmpegConverter",
    "input_format": "mp4",
    "output_format": "webm"
}
```

## Do not edit manually

Changes pushed directly to this repository may be overwritten by the next automated update. If you need to modify the supported conversions, make the change in the originating source repository and let the automation propagate it here.

## URL

The supported conversions data is available at:

```
https://raw.githubusercontent.com/transmute-app/conversion-compatibility/main/supported_conversions.json
```
