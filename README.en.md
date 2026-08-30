# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

## Introduction

Gas Laws Lab is a Windows desktop application for thermal and molecular-motion experiments. It includes standard hard-sphere simulation, ideal-gas relation studies, and air heat-capacity-ratio experiments using both adiabatic expansion and piston oscillation.

This public release repository contains Windows installers, auto-update assets, and multilingual release notes. Reviewed, anonymized source history is published separately in [gas-laws-lab-history](https://github.com/yanshi-qibixunchang/gas-laws-lab-history); private research-report working material is outside that mirror.

## Download and installation

The latest stable release is [`v6.4.0`](https://github.com/yanshi-qibixunchang/gas-laws-lab-release/releases/tag/v6.4.0). Download `heat-capacity-lab-setup-6.4.0.exe` from Releases, verify that it came from this repository, and run it.

Users upgrading from 6.3.1 do not need to uninstall first. Version 6.4.0 retains the application ID, installer identity, update repository, and `C:\Users\<username>\AppData\Roaming\hard-sphere-lab` user-data directory. Durable Free plans, saved traces, parameter snapshots, selections, answers, fitting, calculations, and process evidence continue to restore without regenerating historical experiments under new parameters.

Data written by the withdrawn experimental 5.1.2 build remains outside the compatibility guarantee. Back up the user-data directory before following any recovery instructions.

## Auto update

Open **Help → About** and click **Check for Updates**. A stable update requires all three matching files in the same GitHub Release:

- `heat-capacity-lab-setup-6.4.0.exe`
- `heat-capacity-lab-setup-6.4.0.exe.blockmap`
- `latest.yml`

If automatic update fails, download the latest installer and install it over the existing copy. An uninstall is not required unless a Release explicitly documents an incompatibility.

## Experiment modules

### Heat-capacity ratio by adiabatic expansion

Demo, Guide, and Free modes cover zeroing, pumping, waiting, rapid release, recovery, U₀/U₁/U₂ records, multi-group experiments, calculation, scoring, process review, and report export.

### Heat-capacity ratio by piston oscillation

Version 6.4.0 completes the course-result loop on top of the continuous thermal, sensor, and virtual-hand acquisition model stabilized in 6.3.1:

- Free Mode adds per-experiment process review and scoring. Switching the experiment number updates its instrument timeline, formal trace, selected period, evidence, and expandable score details together.
- Ordinary actions and major saved-curve milestones reuse the established heat-capacity colors, nodes, and tooltip treatment. Re-presses, resets, bottom impacts, hose and power actions, and two-hand release gaps appear only when they actually occurred.
- Completed Free experiments can export a compact PDF report covering the file, recorded measurements, periods, fit, final calculation, process evidence, and scores without a separate theory or formula chapter.
- The Free-mode parameter sidebar exposes ambient pressure and temperature, sampling, the falling trigger, and input visualization. Reviewed advanced parameters require explicit confirmation, and the complete profile freezes with the experiment file after its first formal trace is saved.
- The allowed falling-trigger range scales with ambient pressure while retaining the reviewed `96–130 kPa` window at standard conditions and staying inside sensor limits.
- Acquisition remains pausable, saveable, and retryable after process-review integration, including monitoring after a press that misses the trigger.

### Standard and ideal-gas simulations

Standard Simulation provides hard-sphere molecular motion, realtime sampling, and result charts. Ideal Gas supports `P-T`, `P-V`, and `P-N` scans, fitting, and verification.

## Release notes and validation

- `CHANGELOG.md`: user-facing version history.
- `docs/releases/release-notes.json`: structured trilingual notes used by the in-app update window.
- GitHub Releases: installers, update metadata, and complete notes for each version.

Version 6.4.0 passed TypeScript checks, all `279` automated test files, the production dependency audit, license and exporter-resource consistency checks, and Windows installer plus auto-update asset verification.

## FAQ

**Will upgrading remove old experiments?**  
A normal 6.3.1 → 6.4.0 in-place upgrade reuses the existing user-data directory and preserves durable experiments and historical model snapshots. A backup is still recommended before important classes.

**Why does Realtime Data show only “Power off”?**  
This is the normal off state in the piston-oscillation experiment. Press the power control on the 3D instrument first.

**What if auto update fails?**  
Download the 6.4.0 installer from Releases and install it over the existing copy while retaining the user-data directory.

**Why might Windows show a safety warning?**  
Windows may warn about internet-downloaded installers that have not accumulated enough reputation. Verify the repository URL and Release file name before continuing.
