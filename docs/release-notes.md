# Release Notes

## v1.0.18 (2025-12-14)
**GUI Enhancements & Batch Editing**

### New Features
-   **Batch Edit (Compare & Plan)**: Added batch editing controls to the "Compare & Plan" tab. You can now bulk update the "Plan Start" and "Plan Status" for multiple selected services. ([View Commit](#))
-   **Display Name in Compare**: Added the "Display Name" column to the comparison grid for easier service identification. ([View Commit](#))
-   **Optimized Window**: Resized the GUI window (900x600) to fit perfectly on 14" laptop screens with 150% scaling. ([View Commit](#))

### UI/UX Improvements
-   **Visual Cues**: 
    -   "Restore" button is now **Red** (Caution).
    -   "Save" buttons are now consistent **Green** (Safe).
-   **Dark Mode**: Improved visibility for Dropdowns, Tab Headers, and Column Headers in dark OS themes.
-   **Selection**: Enabled "Extended" selection in the Compare grid to support batch operations.

### Bug Fixes
-   Fixed a script error where `DisplayName` was being added as a duplicate member, causing crashes during comparison updates.
-   Ensured "Save As" dialogs automatically append a timestamp to the filename.

---

## v1.0.12
### Features
-   **GUI Interface**: Added `ServiceManagerGUI.ps1` for easy management of configurations.
-   **Structure**: Organized project into `configs/` (references) and `exports/` (snapshots).
-   **AI Guide**: Added `docs/ai-optimization-guide.md` with prompts for optimizing services.

### Changes
-   Default export location changed to `./exports`.
-   Documentation moved to `./docs`.

## v1.0.2
### Features
-   **Export Mode**: Added ability to export service states (StartType, Status) to JSON.
-   **Restore Mode**: Added ability to restore service states from JSON configuration files.
-   **Filtering**: implemented `-ServiceNames` parameter to target specific services during export.
-   **State Management**: Script now accurately manages `Set-Service` for Startup Types and `Start/Stop-Service` for running status.

### Changes
-   Renamed script from `ListServices.ps1` to `ManageServices.ps1` to reflect expanded capabilities.
-   Output format changed from textual table to structured JSON.
