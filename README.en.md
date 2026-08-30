# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

## Introduction

Gas Laws Lab is a Windows desktop application for thermal and molecular-motion experiments. It includes standard hard-sphere simulation, ideal-gas relation studies, and air heat-capacity-ratio experiments using both adiabatic expansion and piston oscillation.

This is the public release repository. It contains installers, auto-update assets, and multilingual release notes only. Application source is maintained separately in the access-controlled [hard-sphere-lab-1](https://github.com/yanshi-qibixunchang/hard-sphere-lab-1) repository, which may require authorization.

## Download and installation

The latest stable release is [`v6.3.1`](https://github.com/yanshi-qibixunchang/gas-laws-lab-release/releases/tag/v6.3.1). Download `heat-capacity-lab-setup-6.3.1.exe` from Releases, verify that it came from this repository, and run it.

Users upgrading from 6.3.0 do not need to uninstall first. Version 6.3.1 retains the application ID, installer identity, update repository, and `C:\Users\<username>\AppData\Roaming\hard-sphere-lab` user-data directory. Do not clear that directory before upgrading. Durable Free plans, saved curves, selections, drafts, answers, fitting, calculations, and historical model snapshots continue to restore without reinterpretation.

Data written by the withdrawn experimental 5.1.2 build is outside the compatibility guarantee. If old data prevents startup, back up the user-data directory before following the recovery instructions in the Release notes; do not delete the only copy of the data.

## Auto update

Open **Help → About** and click **Check for Updates**. A stable update requires all three matching files in the same GitHub Release:

- `heat-capacity-lab-setup-6.3.1.exe`
- `heat-capacity-lab-setup-6.3.1.exe.blockmap`
- `latest.yml`

If automatic update fails, download the latest installer and install it over the existing copy. An uninstall is not required unless a Release explicitly documents an incompatibility.

## Experiment modules

### Heat-capacity ratio by adiabatic expansion

Demo, Guide, and Free modes cover zeroing, pumping, waiting, rapid release, recovery, U₀/U₁/U₂ records, multi-group experiments, calculation, scoring, process review, and report export.

### Heat-capacity ratio by piston oscillation

Version 6.3.1 closes the data-quality and presentation loop on top of the continuous thermal, sensor, and virtual-hand chain introduced in 6.3.0:

- A whole trace with no credible primary half-cycle reacquires only the affected run while preserving evidence, acquisition settings, and other runs. A usable trace with a narrow selection asks only for reselection.
- Free Mode validates `t1`, `t2`, and `T` together, then validates fitted `A`, `gamma`, and relative error together. Visible inputs stay editable, and malformed drafts are not counted as formal errors.
- Seeded late-trace folds and peak/trough shoulder attenuation make late selection quality matter while preserving the early waveform, `1000 Hz` time grid, underlying thermomechanical trajectory, and sample-for-sample persistence.
- New experiments use one versioned `1.1 N·s/m` equivalent loss for pressing and free oscillation. Historical saves retain their captured `0.434 N·s/m` or other supported snapshot.
- Unequal hand-release timing produces a short-lived side-contact loss without lifting the platform after one hand releases, changing gas stiffness, or adding permanent friction.
- A `0.300 s` presentation delay and `0.55x` pacing over the first `0.400 s` of physical trace give the operator time to pause without changing samples, timestamps, periods, or calculations.
- Live monitoring and audio now recover after a press that misses the trigger, and longer unified-validation button labels no longer overflow.

### Standard and ideal-gas simulations

Standard Simulation provides hard-sphere molecular motion, realtime sampling, and result charts. Ideal Gas supports `P-T`, `P-V`, and `P-N` scans, fitting, and verification.

## Release notes and licenses

- `CHANGELOG.md`: user-facing release history.
- `docs/releases/release-notes.json`: structured trilingual notes used by the in-app update window.
- GitHub Releases: installers, update metadata, and complete notes for each release.

Complete third-party licenses, audio sources, and model records for 6.3.1 are available inside the app. All `276` test files pass, third-party dependency records are verified, the production audit reports `0 vulnerabilities`, and all three desktop update assets pass consistency checks before publication.

## FAQ

**Will upgrading remove old experiments?**  
A normal 6.3.0 → 6.3.1 in-place upgrade reuses the existing user-data directory and preserves durable Free data and historical model snapshots. A backup is still recommended before important classes or experiments.

**Why does Realtime Data show only “Power off”?**  
This is the normal off state in the piston-oscillation experiment. Press the power control on the 3D instrument first.

**What if auto update fails?**  
Download the 6.3.1 installer from Releases and install it over the existing copy while retaining the user-data directory.

**Why might Windows show a safety warning?**  
Windows may warn about internet-downloaded installers that have not accumulated enough reputation. Verify the repository URL and Release file name before continuing.
