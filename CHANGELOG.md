# Changelog

## 5.1.2

- Builds on 5.1.1 with precise recovery for valid legacy workspaces, never-reused internal experiment IDs, complete Free, Guide, and Demo records, and strict post-commit save verification.
- Stabilizes mode switching, reminder and tick lifecycles, WebGL recovery, and numeric boundaries so normal experiment runs do not produce transient save failures.
- Adds update recovery to the read-only persistence failure page and retains the existing appId, NSIS identity, update repository, and `hard-sphere-lab` user-data directory.
- Introduces the localized 气律实验室, 氣律實驗室, and Gas Laws Lab names plus the new Windows and web application icon.

## 4.1.7

- Publishes the first acceptance release from the public release repository.
- Adds Help > User Guide in the desktop app, opening the language-appropriate public README for download, update, experiment workflow, and FAQ instructions.
- Keeps the public repository limited to release documentation and update assets; application source code remains excluded.

## 4.1.6

- Migrates the desktop auto-update channel so future update assets and release notes are published from the new public release repository.
- Keeps the `4.1.6` installer available through the old source repository so installed `4.1.5` clients can detect only the migration release.
- Clarifies that the public release repository provides installers, update metadata, and release notes only, without application source code.
