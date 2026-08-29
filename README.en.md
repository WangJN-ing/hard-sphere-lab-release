# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

## Introduction

Gas Laws Lab is a Windows desktop application for thermal and molecular-motion experiments. It includes standard hard-sphere simulation, ideal-gas relation studies, and air heat-capacity-ratio experiments using both adiabatic expansion and piston oscillation.

This is the public release repository. It contains installers, auto-update assets, and multilingual release notes only. The application source is available in the public [hard-sphere-lab-1](https://github.com/WangJN-ing/hard-sphere-lab-1) repository.

## Download and installation

The latest stable release is [`v6.3.0`](https://github.com/WangJN-ing/hard-sphere-lab-release/releases/tag/v6.3.0). Download `heat-capacity-lab-setup-6.3.0.exe` from Releases, verify that it came from this repository, and run it.

Users upgrading from 6.2.1 do not need to uninstall first. Version 6.3.0 retains the application ID, installer identity, update repository, and `C:\Users\<username>\AppData\Roaming\hard-sphere-lab` user-data directory. Do not clear that directory before upgrading. Durable Free plans, saved curves, selections, drafts, answers, fitting, and calculations continue to restore.

Data written by the withdrawn experimental 5.1.2 build is outside the compatibility guarantee. If old data prevents startup, back up the user-data directory before following the recovery instructions in the Release notes; do not delete the only copy of the data.

## Auto update

Open **Help → About** and click **Check for Updates**. A stable update requires all three matching files in the same GitHub Release:

- `heat-capacity-lab-setup-6.3.0.exe`
- `heat-capacity-lab-setup-6.3.0.exe.blockmap`
- `latest.yml`

If automatic update fails, download the latest installer and install it over the existing copy. An uninstall is not required unless a Release explicitly documents an incompatibility.

## Experiment modules

### Heat-capacity ratio by adiabatic expansion

Demo, Guide, and Free modes cover zeroing, pumping, waiting, rapid release, recovery, U₀/U₁/U₂ records, multi-group experiments, calculation, scoring, process review, and report export.

### Heat-capacity ratio by piston oscillation

Version 6.3.0 expands Free Mode and repairs the Guide experience:

- Free Mode adds a continuous thermal, pressure-sensor, press, and virtual-hand acquisition chain. Each height retains its own equilibrium and settling behavior, while the display clock, raw samples, and processed data share one time base.
- Power, hose connection and removal, locking-screw motion, piston vibration, and bottom impact now have state-aligned audio. Height resets in applicable modes follow the actual drop, while movement below `5 mm` remains silent.
- The Guide checklist, primary controls, and interaction gates read one effective step, so a correct action after a reminder is not rejected by stale conditions.
- At `0.500 s`, recording freezes the curve and time before Pause becomes available. The gate accounts for the distinct modeled settling offsets at `80 / 70 / 60 mm`.
- Internal baseline steps from old saves migrate automatically and cannot reappear. Sample-rate and threshold fields accept Enter consistently.
- Guide and Demo display crisp clockwise or counterclockwise screw arrows, tolerate correct-direction hand motion beyond the completion threshold, and use gentle correction followed by boundary protection for reverse motion.
- Demo height adjustment, hose removal, and hose connection now take `50%` of their previous duration.

### Standard and ideal-gas simulations

Standard Simulation provides hard-sphere molecular motion, realtime sampling, and result charts. Ideal Gas supports `P-T`, `P-V`, and `P-N` scans, fitting, and verification.

## Release notes and licenses

- `CHANGELOG.md`: user-facing release history.
- `docs/releases/release-notes.json`: structured trilingual notes used by the in-app update window.
- GitHub Releases: installers, update metadata, and complete notes for each release.

Complete third-party licenses, audio sources, and model records for 6.3.0 are available inside the app. All `272` test files pass, `468` dependency records are verified, the production audit reports `0 vulnerabilities`, and all three desktop update assets pass consistency checks before publication.

## FAQ

**Will upgrading remove old experiments?**  
A normal 6.2.1 → 6.3.0 in-place upgrade reuses the existing user-data directory and preserves durable Free data. A backup is still recommended before important classes or experiments.

**Why does Realtime Data show only “Power off”?**  
This is the normal off state in the piston-oscillation experiment. Press the power control on the 3D instrument first.

**What if auto update fails?**  
Download the 6.3.0 installer from Releases and install it over the existing copy while retaining the user-data directory.

**Why might Windows show a safety warning?**  
Windows may warn about internet-downloaded installers that have not accumulated enough reputation. Verify the repository URL and Release file name before continuing.
