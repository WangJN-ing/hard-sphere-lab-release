# Gas Laws Lab

## Project Introduction

Gas Laws Lab is a desktop application for heat capacity ratio experiments, standard molecular simulation, and ideal gas relationship verification. It provides 3D previews, real-time data, parameter controls, experiment records, process review, and result calculation.

This repository is the public release repository. It is used only for installers, auto-update assets, and release notes; it does not contain the application source code.

## Download And Installation

Download the latest non-prerelease version from this repository's GitHub Releases page unless a course or maintainer instructs otherwise.

The latest stable release is `v5.1.2`. A normally running 5.1.1 installation can check for and install the update in-app. If 5.1.1 is already on the read-only persistence failure page, download the 5.1.2 installer from Releases and install it over the existing copy.

The Windows installer uses the file name pattern `heat-capacity-lab-setup-x.y.z.exe`. After downloading it, run the installer to install the app or install over an existing version.

Do not uninstall the previous version or clear `C:\Users\<username>\AppData\Roaming\hard-sphere-lab` when upgrading. Version 5.1.2 retains the existing appId, installer identity, update repository, and user-data directory.

## Auto Update

Installed desktop clients can check for updates inside the app. Auto update requires the same GitHub Release to include `latest.yml`, the installer `.exe`, and the `.exe.blockmap` file.

If auto update fails, download the latest installer manually from this repository's Releases page and install it over the existing version.

## Main Workflow

1. Create or open an experiment file.
2. Select the experiment file in the left sidebar and open the required experiment panel.
3. Adjust the current experiment parameters in the right sidebar.
4. Run the experiment in the center workspace, and view the 3D preview, real-time data, and charts.
5. Record data, inspect relationship curves, or complete sampling according to the experiment type.
6. After the experiment is complete, open Results, Data Processing, or Process Review from the left sidebar.
7. The bottom console shows runtime information, save messages, warnings, and action feedback in real time.

## Experiment Modules

### Heat Capacity Ratio Experiment

The heat capacity ratio experiment supports demonstration, guided, and free workflows. In free experiments, users can adjust experiment parameters and complete the high-level process of pumping, warm-up or recovery, valve release, and final recovery.

Key data can be recorded during the experiment. Process Review shows the measured curve, ideal reference curve, stage timeline, and record window for reviewing the run. The Results page calculates the heat capacity ratio and displays error or score information.

### Standard Simulation

Standard Simulation provides hard-sphere molecular simulation for real-time observation, sampled data collection, and result charts.

### Ideal Gas Simulation

Ideal Gas Simulation supports `P-T`, `P-V`, and `P-N` relationship verification. Users can generate data points with the relation selector, scan variable, and sampling preset, then review the relationship verification results.

## Core Features

- Parameter adjustment
- 3D preview
- Real-time data and charts
- Data recording
- Result calculation
- Process review
- Multilingual UI
- Light and dark modes
- Desktop auto update

## Version Notes

Version notes are available in `CHANGELOG.md`, `docs/releases/release-notes.json`, and GitHub Releases.

Release notes are available in Simplified Chinese, Traditional Chinese, and English.

## Repository Structure

```text
README.md
  Simplified Chinese download, update, and usage guide.

README.zh-TW.md
  Traditional Chinese download, update, and usage guide.

README.en.md
  English download, update, and usage guide.

CHANGELOG.md
  Human-readable version history.

docs/releases/release-notes.json
  Structured multilingual release notes used by the release process and update dialog.

GitHub Releases
  Installer, latest.yml, and blockmap assets for each release.
```

## FAQ

**Where do I download the app?**  
Download the latest non-prerelease installer from this repository's GitHub Releases page.

**What should I do if auto update fails?**  
Download the latest `heat-capacity-lab-setup-x.y.z.exe` manually and install it over the existing version.

**Why might Windows show a safety warning?**  
Windows may show a safety prompt for installers downloaded from the internet. Confirm that the installer came from this repository's Releases page before continuing.

**How do I check the current app version?**  
Open the app's About or version information entry to view the current version.

**Does this repository contain source code?**  
No. This repository only provides release assets, auto-update files, and version notes.

**Where can I read release notes?**  
Read `CHANGELOG.md`, `docs/releases/release-notes.json`, or the corresponding GitHub Release page.
