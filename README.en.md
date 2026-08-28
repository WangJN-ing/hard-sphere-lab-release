# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

## Introduction

Gas Laws Lab is a Windows desktop application for thermal and molecular-motion experiments. It includes standard hard-sphere simulation, ideal-gas relation studies, and air heat-capacity-ratio experiments using both adiabatic expansion and piston oscillation.

This is the public release repository. It contains installers, auto-update assets, and multilingual release notes only. The application source is available in the public [hard-sphere-lab-1](https://github.com/WangJN-ing/hard-sphere-lab-1) repository.

## Download and installation

The latest stable release is [`v6.2.1`](https://github.com/WangJN-ing/hard-sphere-lab-release/releases/tag/v6.2.1). Download `heat-capacity-lab-setup-6.2.1.exe` from Releases, verify that it came from this repository, and run it.

Users upgrading from 6.2.0 do not need to uninstall first. Version 6.2.1 retains the application ID, installer identity, update repository, and `C:\Users\<username>\AppData\Roaming\hard-sphere-lab` user-data directory. Do not clear that directory before upgrading. Existing selections, Free plans, saved curves, drafts, answers, fitting, and calculations continue to restore.

Data written by the withdrawn experimental 5.1.2 build is outside the compatibility guarantee. If old data prevents startup, back up the user-data directory before following the recovery instructions in the Release notes; do not delete the only copy of the data.

## Auto update

Open **Help → About** and click **Check for Updates**. A stable update requires all three matching files in the same GitHub Release:

- `heat-capacity-lab-setup-6.2.1.exe`
- `heat-capacity-lab-setup-6.2.1.exe.blockmap`
- `latest.yml`

If automatic update fails, download the latest installer and install it over the existing copy. An uninstall is not required unless a Release explicitly documents an incompatibility.

## Experiment modules

### Heat-capacity ratio by adiabatic expansion

Demo, Guide, and Free modes cover zeroing, pumping, waiting, rapid release, recovery, U₀/U₁/U₂ records, multi-group experiments, calculation, scoring, process review, and report export.

### Heat-capacity ratio by piston oscillation

Version 6.2.0 completes Free Mode on top of the existing Demo and Guide workflows and unifies the instrument state and loaded-equilibrium model across all three modes. Version 6.2.1 is the stability patch for acquisition, selection, rebound, and recovery.

- Fixes the first-press white screen while the formal curve is still incomplete, keeping live plotting, pause, and save continuous.
- Fixes selection-result formatting and restores bigint-shaped values from earlier saves without changing selection gestures, endpoints, period rules, or precision.
- Removes unsupported fixed rebound-velocity ranges, so normal peaks above 2 m/s are neither clipped nor misreported while all other physical and divergence checks remain.
- Restores visible screw-release settling. Genuine animation-runtime failures silently return to the current stable position and retain data.
- Contains processing or calculation render errors inside the content region, while outer failures retain the real desktop window controls.
- Clears only non-resumable press, hold, free-fall, rebound, and short-animation state on restart while preserving durable Free work.

- Free Mode supports 3–6-run plans, system heights, and unlimited integer custom candidates from 10 to 80 mm, progressing from higher to lower targets.
- Every run independently stores its 1–1000 Hz sample rate, 96.0–130.0 kPa falling threshold, raw samples, period selection, answer history, and physical snapshot. The monitor keeps both the threshold and curve visible.
- Leaving the mode, reloading, or reopening the file resumes the same session. The progress menu supports retry, deletion, and whole-session reset; final period verification opens fitting and calculation automatically.
- Closing calculation restores the 3D instrument and realtime-data layout, while historical processing reopens from the sidebar. Materials navigation adapts to Demo, Guide, and Free.
- Releasing the locking screw produces a smooth one-way 0.2 s settling motion to the real loaded equilibrium. Nominal height remains learner-facing while exact height and gas state are generated and persisted internally.
- Demo, Guide, and Free continue to share power gating, hose, screw, platform, acquisition, and calculation behavior, with repaired transitions, exit semantics, screw visual travel, and processing return.

### Standard and ideal-gas simulations

Standard Simulation provides hard-sphere molecular motion, realtime sampling, and result charts. Ideal Gas supports `P-T`, `P-V`, and `P-N` scans, fitting, and verification.

## Release notes and licenses

- `CHANGELOG.md`: user-facing release history.
- `docs/releases/release-notes.json`: structured trilingual notes used by the in-app update window.
- GitHub Releases: installers, update metadata, and complete notes for each release.

The 6.2.1 installer includes 468 classified dependency-license records, with complete third-party licenses and model-source records available inside the app. All 261 test files passed, and the production-dependency audit reported zero vulnerabilities at release time.

## FAQ

**Will upgrading remove old experiments?**  
A normal 6.2.0 → 6.2.1 in-place upgrade reuses the existing user-data directory and preserves durable Free data. A backup is still recommended before important classes or experiments.

**Why does Realtime Data show only “Power off”?**  
This is the normal off state in the piston-oscillation experiment. Press the power control on the 3D instrument first.

**What if auto update fails?**  
Download the 6.2.1 installer from Releases and install it over the existing copy while retaining the user-data directory.

**Why might Windows show a safety warning?**  
Windows may warn about internet-downloaded installers that have not accumulated enough reputation. Verify the repository URL and Release file name before continuing.
