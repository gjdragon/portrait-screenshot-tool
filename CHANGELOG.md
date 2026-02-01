# Changelog
All notable changes to this project will be documented in this file.


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
