# Changelog
All notable changes to this project will be documented in this file.

## [1.8.0] - 2026-02-07

### Added
- **Separate Memory for Portrait and Landscape Modes**: The application now remembers the last captured region independently for portrait (9:16) and landscape (16:9) modes
  - When you switch to portrait mode, it will restore the last position you used in portrait mode
  - When you switch to landscape mode, it will restore the last position you used in landscape mode
  - This allows you to have different preferred capture areas for different aspect ratios

### Changed
- **Improved Mode Switching**: Switching between portrait and landscape modes now properly applies default dimensions
  - Portrait mode (9:16): Automatically sets to 607×1080 pixels
  - Landscape mode (16:9): Automatically sets to 1920×1080 pixels
  - Both radio buttons (Portrait and Landscape) are now properly connected to handle mode changes

### Fixed
- Fixed issue where landscape mode dimensions were not updating correctly when switching from portrait mode
- Fixed radio button handler that was only connected to the portrait button, causing landscape mode to be unresponsive

### Technical Details
- Settings storage now uses `last_capture_rect_9:16` for portrait mode regions
- Settings storage now uses `last_capture_rect_16:9` for landscape mode regions
- Legacy `last_capture_rect` key is deprecated but won't affect existing installations

---


## [1.7.0] - 2026-02-01

1. **File Prefix Setting (Optional)**
   - Added a new "File prefix" field in the UI
   - **Default behavior**: Leave empty to use timestamp naming (original feature preserved)
   - **Custom prefix**: Enter a prefix like "picture", "screenshot", "image" to use sequential numbering

2. **Two Naming Modes**

   **Mode 1: Timestamp (Default - when prefix is empty)**
   - Filenames: `Portrait_2024-02-01_14-30-45.png`
   - This is the original behavior - keeps working as before
   
   **Mode 2: Sequential Numbering (when you enter a prefix)**
   - Filenames: `{prefix}1.png`, `{prefix}2.png`, `{prefix}3.png`, etc.
   - For example, with prefix "picture": `picture1.png`, `picture2.png`, `picture3.png`

3. **Smart Sequence Detection**
   - When using a custom prefix, the app scans the save folder
   - Finds the highest number used with your current prefix
   - Automatically uses the next number in sequence
   - If you delete old screenshots, the numbering adjusts dynamically

## [1.6.0] - 2026-02-01

1. **File Prefix Setting**
   - Added a new "File prefix" field in the UI where users can specify a custom prefix for screenshot filenames
   - Default prefix is "Portrait"
   - Users can change it to anything like "picture", "screenshot", "image", etc.

2. **Auto-Incrementing Sequence Numbers**
   - Screenshots now save as: `{prefix}1.png`, `{prefix}2.png`, `{prefix}3.png`, etc.
   - For example, with prefix "picture": `picture1.png`, `picture2.png`, `picture3.png`

3. **Smart Sequence Detection**
   - The app scans the save folder every time you take a screenshot
   - It finds the highest number used with your current prefix
   - Automatically uses the next number in sequence
   - If you delete old screenshots, the numbering adjusts dynamically

## [1.5.0] - 2025-12-25
### Changed
- Reorganize project structure to be more GitHub-friendly
- Move `main.py` into the `src/` directory

### Added
- Application icon (`icon.ico`)
- Screenshot (`screenshot.png`) under `res/`

---

## [1.4.0] - 2025-12-07
### Added
- Resizable capture rectangle with live dimension updates
- Visual region overlay during selection
- Dynamic width and height display

---

## [1.3.0] - 2025-12-07
### Added
- Clipboard copy option via checkbox

---

## [1.2.0] - 2025-12-07
### Added
- Auto-dismissing toast notifications
- Improved overlay visibility by dimming only outside the capture area

---

## [1.1.0] - 2025-12-07
### Added
- Region memory to restore the last capture location

---

## [1.0.0] - 2025-11-15
### Added
- Initial beta release
