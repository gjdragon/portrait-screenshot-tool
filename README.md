# Portrait Screenshot Tool

A lightweight, customizable screenshot utility designed for capturing content in portrait or landscape aspect ratios - perfect for creating content for YouTube Shorts, TikTok, Instagram Reels, or standard video formats.

![Screenshot Tool Demo](demo.gif) <!-- Add a demo gif if you have one -->

## Features

- 🎯 **Custom aspect ratios**: 9:16 (portrait) or 16:9 (landscape) with lock option
- ⌨️ **Global hotkey support**: Capture from anywhere with customizable keyboard shortcuts
- 🖼️ **Visual overlay**: Live preview of capture area with drag-to-position
- 💾 **Auto-save**: Automatically saves with timestamp to your chosen directory
- 🔔 **System tray integration**: Runs quietly in the background
- 🖥️ **Multi-monitor support**: Works seamlessly across multiple displays
- 🎨 **Customizable dimensions**: Set any width/height you need

## Installation

### Prerequisites

- Python 3.7 or higher
- PyQt5
- keyboard library

### Setup

1. Clone this repository:
```bash
git clone https://github.com/yourusername/portrait-screenshot-tool.git
cd portrait-screenshot-tool
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python v5-ratio-option.py
```

### Platform-Specific Notes

**Linux**: You may need to run with sudo for keyboard hooks:
```bash
sudo python v5-ratio-option.py
```

**macOS**: Grant accessibility permissions when prompted.

**Windows**: Should work out of the box. Run as administrator if hotkeys don't work.

## Usage

### Quick Start

1. Launch the application
2. Configure your preferred settings (optional)
3. Press the hotkey (`Ctrl+Shift+P` by default) or click "Capture Now"
4. Drag the purple rectangle to position it over your desired capture area
5. Press `Enter` to capture, or `Esc` to cancel

### Settings

- **Hotkey**: Customize the keyboard shortcut (e.g., `ctrl+shift+p`, `ctrl+alt+s`)
- **Save Location**: Choose where screenshots are saved
- **Dimensions**: Set custom width and height
- **Lock Aspect Ratio**: Maintain 9:16 or 16:9 ratio automatically
- **Ratio Mode**: Toggle between portrait (9:16) and landscape (16:9)

### Keyboard Shortcuts in Overlay

- `Enter` - Capture screenshot
- `Esc` - Cancel capture
- Click and drag - Reposition capture area

## Configuration

Settings are automatically saved to `~/.portrait_screenshot_settings.json`

Default settings:
```json
{
  "hotkey": "ctrl+shift+p",
  "save_location": "~/Screenshots",
  "portrait_width": 608,
  "portrait_height": 1080,
  "lock_ratio": true,
  "ratio_mode": "9:16"
}
```

## Common Use Cases

- **YouTube Shorts**: Use 9:16 ratio with 1080x1920 dimensions
- **TikTok/Instagram Reels**: Use 9:16 ratio with 1080x1920 dimensions
- **YouTube Videos**: Use 16:9 ratio with 1920x1080 dimensions
- **Custom Content**: Unlock ratio and set any dimensions you need

## Troubleshooting

**Hotkey not working**: 
- Try running with administrator/sudo privileges
- Check if another application is using the same hotkey
- Try a different hotkey combination

**Screenshots saving to wrong location**:
- Check the "Save to" path in settings
- Ensure the directory has write permissions

**Overlay not appearing**:
- Check if the application is running in system tray
- Try clicking "Capture Now" from the main window
- Restart the application

## Development

Built with:
- PyQt5 - GUI framework
- keyboard - Global hotkey support
- Python 3.7+

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Known Limitations

- Keyboard hooks may require elevated permissions on some systems
- macOS may require accessibility permissions
- Global hotkeys may conflict with other applications

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by the need for quick portrait-oriented screenshots
- Built for content creators working with vertical video formats

## Support

If you encounter any issues or have suggestions, please [open an issue](https://github.com/yourusername/portrait-screenshot-tool/issues).

---

**Star this repo if you find it useful!** ⭐