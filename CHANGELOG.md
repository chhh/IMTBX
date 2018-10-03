# IMTBX+Grppr

## Contents

- `IMTBX_v5.x.x.zip` - Everyting in one package: data viewer, peak detector, UI for starting the peak detector and isotopic grouping.
- `grppr-0.3.xx.jar` - Only the Grppr java program.

## Changelog

### v5.0.1
- IMTBX update to v5.0.1
  - Important fix for scan Averaging mode, was broken for files with many functions in them.
  - Viewer fix for closing files properly.
- Grppr update to v0.3.21
  - Fix for multi-digit function names.
  - Recognize function number '0' as the default for all functions for '-d' deisotoping
  option. This allows deisotoping of files with unknown number of functions.
  - Fix MS1/MS2 grouping deisotoping config to allow functions other than 1/2 to be used.

### v4.4.5
- IMTBX update to v4.5.0
  - Option to skip some errors with mass calibration.
- Grppr update to v0.3.20
  - Several new options
  - Bugfixes

### v4.4.1

- IMTBX update to v4.3.0
  - Final fixes for calibration reading in older instruments.
  - Allow calibration coefficients to only be scpeficied for one
  function in HEADER.txt, they will be duplicated to other functions.
  - Code duplicates removed, all reading of coefficients moved to
  a single location.

### v4.4.0

- Grppr update to v0.3.15
  - Fix Grppr crashing when input contained some clusters of 1, 2 or 3 peaks that had to be truncated.

### v4.3.1

- IMTBX update to v4.2.0
  - Can accept 5 or 6 calibration coefficients in headers.txt

### v4.3.0

- Add `--allOut` option to Grppr to allow writing _*.isotopes_ files along with MGF.
- Add a checkbox to GUI Grppr LCMS-Only section for --allOut.
- Restore last state of the GUI form upon reopening.
- Another fix for how `-d` deisotoping options were passed from GUI to Grppr.

### v4.2.0

- Some bugfixes for IMTBX+Grppr GUI, not all parameters were passed on properly.
- Decrease lower mass boundary for AVERAGINE isotopic cluster detector to 50 from 200. Helps with small molecules if AVERAGINE is by accident used for them.