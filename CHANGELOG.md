# Changelog
Script versions for this beta repository. Script versions are numbered separately from the paid kit (guide) versions; the matching kit version is listed for each release. The scripts in each release are byte-identical to the ones in the matching paid kit.

## 2026-10-16: repository split (scripts 1.2.2, Kit 2 v1.3.2)
- Moved from the combined `zakopenc/deployment-doctor-beta` repo (now archived) into this repo. Script files are unchanged; only the folder layout, README, tests' paths and sample report changed.
- The test that checked KC IDs against the paid guide source was removed, since the guide isn't in this repo.

## 2026-10-16: scripts 1.2.2 (Kit 2 v1.3.2)
- Tenant pre-check: each app is checked in its own try/catch; an app that can't be evaluated gets a Warning finding (T00) and the rest of the run still writes a report.
- One PSScriptAnalyzer unused-parameter warning fixed. KC-004 and T09 relabelled Multi-source in `known-causes.json` (v1.2.1).
- HTML report: Scope and Check columns no longer break words mid-word.

## 2026-10-16: scripts 1.2.1 (Kit 2 v1.3.1)
- Report: Kit 2 branding, real status with a separate Confidence column, the analysed log source shown for `-LogPath`, and no "live tenant" wording on the device banner.

## 2026-10-16: scripts 1.2.0 (Kit 2 v1.3.0)
- HTML dashboard report: health score, status cards, filters, light/dark themes, print layout, `-NoHtml`. Any Critical finding caps the score at 49.

## 2026-10-16: first beta release (scripts 1.2.0, Kit 2 v1.2.0)
- Read-only scripts with Pester tests.
