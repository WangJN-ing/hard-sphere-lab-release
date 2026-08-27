# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

## Introduction

Gas Laws Lab is a Windows desktop application for thermal and molecular-motion experiments. It includes standard hard-sphere simulation, ideal-gas relation studies, and air heat-capacity-ratio experiments using both adiabatic expansion and piston oscillation.

This is the public release repository. It contains installers, auto-update assets, and multilingual release notes only. The application source is available in the public [hard-sphere-lab-1](https://github.com/WangJN-ing/hard-sphere-lab-1) repository.

## Download and installation

The latest stable release is [`v6.1.1`](https://github.com/WangJN-ing/hard-sphere-lab-release/releases/tag/v6.1.1). Download `heat-capacity-lab-setup-6.1.1.exe` from Releases, verify that it came from this repository, and run it.

Users upgrading from 5.3.1 normally do not need to uninstall first. Version 6.1.1 retains the application ID, installer identity, update repository, and `C:\Users\<username>\AppData\Roaming\hard-sphere-lab` user-data directory. Do not clear that directory before upgrading. The release gate performs a 5.3.1 → 6.1.1 same-path replacement, profile-preservation, launch, and error check on a fresh temporary Windows machine.

Data written by the withdrawn experimental 5.1.2 build is outside the compatibility guarantee. If old data prevents startup, back up the user-data directory before following the recovery instructions in the Release notes; do not delete the only copy of the data.

## Auto update

Open **Help → About** and click **Check for Updates**. A stable update requires all three matching files in the same GitHub Release:

- `heat-capacity-lab-setup-6.1.1.exe`
- `heat-capacity-lab-setup-6.1.1.exe.blockmap`
- `latest.yml`

If automatic update fails, download the latest installer and install it over the existing copy. An uninstall is not required unless a Release explicitly documents an incompatibility.

## Experiment modules

### Heat-capacity ratio by adiabatic expansion

Demo, Guide, and Free modes cover zeroing, pumping, waiting, rapid release, recovery, U₀/U₁/U₂ records, multi-group experiments, calculation, scoring, process review, and report export.

### Heat-capacity ratio by piston oscillation

Version 6.1.1 adds a complete Demo, a complete Guide, and normal 3D operation. The Free entry remains labelled as not yet available.

- A pressable physical power control combines the sensor and computer-acquisition power states.
- Power must be on before sampling-rate and pressure input, plots, or data recording are available. When off, the **Realtime Data** title remains and the content area shows only **Power off**.
- Guide enforces the current step. Pressing another control produces acknowledgement motion without changing experiment state, followed by a prompt to finish the current step.
- Three runs use 80, 70, and 60 mm heights and cover platform/scale adjustment, screw locking and release, hose disconnect/drag/magnetic reconnection, acquisition, piston release, stop, save, and period selection.
- After period selection, the 3D + realtime layout returns and Guide requires power-off before opening calculation directly.
- Demo plays the complete sequence and powers the instrument off automatically at the end.

### Standard and ideal-gas simulations

Standard Simulation provides hard-sphere molecular motion, realtime sampling, and result charts. Ideal Gas supports `P-T`, `P-V`, and `P-N` scans, fitting, and verification.

## Release notes and licenses

- `CHANGELOG.md`: user-facing release history.
- `docs/releases/release-notes.json`: structured trilingual notes used by the in-app update window.
- GitHub Releases: installers, update metadata, and complete notes for each release.

Version 6.1.1 updates npm, Electron, installer tooling, audio attribution, and 3D-model provenance. Complete third-party licenses and model-source records are distributed with the installer and available inside the app.

## FAQ

**Will upgrading remove old experiments?**  
A normal 5.3.1 → 6.1.1 in-place upgrade reuses the existing user-data directory. A backup is still recommended before important classes or experiments.

**Why does Realtime Data show only “Power off”?**  
This is the normal off state in the piston-oscillation experiment. Press the power control on the 3D instrument first.

**What if auto update fails?**  
Download the 6.1.1 installer from Releases and install it over the existing copy while retaining the user-data directory.

**Why might Windows show a safety warning?**  
Windows may warn about internet-downloaded installers that have not accumulated enough reputation. Verify the repository URL and Release file name before continuing.
