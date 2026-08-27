# Changelog

## 6.1.1

- Adds the complete piston-oscillation heat-capacity-ratio experiment with Demo, Guide, normal 3D operation, three 80/70/60 mm acquisition runs, period processing, and calculation.
- Adds a pressable power control that gates parameter input, realtime plots, and recording; Guide starts with power-on and requires power-off after period selection, while Demo powers off automatically.
- Enforces strict Guide ordering: out-of-step controls animate to acknowledge input but cannot change physical state.
- Replaces the formal piston model with the audited hybrid refinement while preserving functional node, hierarchy, origin, motion-axis, hit-target, magnetic-snap, scale, and camera contracts.
- Updates Electron, js-yaml, PostCSS, installer tooling, generated legal notices, audio attribution, and 3D-model provenance; npm security audits report zero known vulnerabilities at release time.
- Adds a clean-Windows 5.3.1 → 6.1.1 same-path upgrade gate in addition to exact differential blockmap reconstruction.

## 5.3.1

- Completes multi-group adiabatic-expansion experiments with automatic progression, group-level calculation and scoring, process review, and report/figure/package exports.
- Adds separate, confirmed controls for restarting only the current experiment or the current group without discarding other completed groups.
- Improves report hierarchy, three-line tables, scientific figure styling, and Chinese/Latin font consistency.

## 5.2.0

- Moves V3 workspace projection, fingerprinting, generation commits, and read-back verification into a background Worker, while semantic saves use bounded debounce and continuous runs checkpoint at most once every 15 seconds.
- Preserves valid standard, ideal-gas, and heat-capacity workspaces written by 4.2.3 and 5.1.1. Data written by the withdrawn 5.1.2 build is outside the compatibility guarantee.
- Bounds Free traces to 800 samples and 320 detailed events per branch, 4 detailed branches per trial, and 7 completed trials plus the active trial per parameter domain.
- Retries temporary persistence failures, prunes invalid candidates after quota failures, retains the last verified generation, and keeps save errors non-blocking.

## 5.1.2 (withdrawn)

- This experimental build is withdrawn. Its workspace data is outside the compatibility guarantee for later stable versions.

## 4.1.7

- Publishes the first acceptance release from the public release repository.
- Adds Help → User Guide in the desktop app, opening the language-appropriate public README.

## 4.1.6

- Migrates desktop auto updates to the public release repository while keeping the existing installer and user-data identities.
