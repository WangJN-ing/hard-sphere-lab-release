# Changelog

## 6.2.1

- Fixes the first Free acquisition render failure while the formal pressure curve is still incomplete, keeping trigger, live plotting, pause, save, and next-run progression continuous.
- Converts period-selection indices and counts to safe rendering types, including legacy bigint-shaped values, without changing selection gestures, endpoint rules, period verification, or precision.
- Restores the visible screw-release settling motion by redrawing the demand-driven 3D instrument whenever piston, screw, hose, or platform state changes.
- Removes all unsupported fixed rebound-velocity ranges. Normal peaks above 2 m/s remain intact while finite-value, physical-boundary, and numerical-divergence checks continue.
- Silently stops failed rebound or settling animations, recomputes the stable position from current physical conditions, retains experiment data, and prevents a stuck rebounding state.
- Normalizes non-resumable press, hold, free-fall, rebound, and short-animation state on restart while preserving Free plans, curves, drafts, selections, answers, fitting, calculations, and audit history.
- Adds local processing/calculation render recovery that preserves the workbench chrome and data, plus an outer recovery frame that retains the real minimize, maximize/restore, and close controls.
- Verifies 3–6-run and mixed system/custom-height workflows through selection, answer history, automatic calculation, fitting, results, instrument return, persistence, and explicit reset.
- Ships matching installer, blockmap, and update metadata after 261 test files, TypeScript checks, 468-license-record verification, and a production audit with zero known vulnerabilities.

## 6.2.0

- Completes piston-oscillation Free Mode with resumable 3–6-run plans, system and custom 10–80 mm targets, ordered progress, retry, deletion, whole-session reset, period verification, fitting, and automatic calculation handoff.
- Adds per-run 1–1000 Hz sampling and 96.0–130.0 kPa falling-threshold settings, dynamic monitoring ranges, immediate acquisition when the threshold is already met, and complete raw-sample, physical-snapshot, and answer-history records.
- Unifies experiment-count and Free-progress controls across both heat-capacity methods, including keyboard, outside-click, popover placement, reset, color, and destructive-action behavior.
- Makes left-side materials navigation mode-specific and restores the 3D instrument plus realtime-data layout after calculation closes.
- Repairs Demo, Guide, and Free transitions, Free exit semantics, screw visual travel and pointer sensitivity, processing return, and non-blocking startup recovery.
- Applies one loaded-gas equilibrium model across all three piston modes. Screw release produces a recordable one-way 0.2 s settling segment while nominal and exact heights remain distinct.
- Migrates existing piston files into the new Free-session and thermodynamic structures without fabricating missing historical evidence, and prevents the rigid 0 mm lower stop from producing a false savable run.
- Ships matching installer, blockmap, and update metadata after 259 test files, TypeScript checks, 468-license-record verification, and a production audit with zero known vulnerabilities.

## 6.1.1

- Adds the complete piston-oscillation heat-capacity-ratio experiment with Demo, Guide, normal 3D operation, three 80/70/60 mm acquisition runs, period processing, and calculation.
- Adds a pressable power control that gates parameter input, realtime plots, and recording; Guide starts with power-on and requires power-off after period selection, while Demo powers off automatically.
- Enforces strict Guide ordering: out-of-step controls animate to acknowledge input but cannot change physical state.
- Replaces the formal piston model with the audited hybrid refinement while preserving functional node, hierarchy, origin, motion-axis, hit-target, magnetic-snap, scale, and camera contracts.
- Updates Electron, js-yaml, PostCSS, installer tooling, generated legal notices, audio attribution, and 3D-model provenance; npm security audits report zero known vulnerabilities at release time.
- Passes a clean-Windows 5.3.1 → 6.1.1 same-path upgrade gate, including workspace migration and exact differential blockmap reconstruction.

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
