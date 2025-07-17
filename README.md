# LinguaFox

A Firefox extension that uses OpenAI's GPT-4o model to intelligently translate text between Chinese and other languages.

## Features

- **Smart Translation**: Automatically detects input language and translates accordingly:
  - Chinese → English
  - Other languages (English, Korean, Japanese, etc.) → Traditional Chinese (zh-TW)
- **Local Storage**: Securely stores your OpenAI API key and custom system prompt locally
- **Customizable System Prompt**: Tailor the translation behavior to your specific needs

## Installation

1. Clone or download this repository
2. Open Firefox and navigate to `about:debugging`
3. Click "This Firefox" in the left sidebar
4. Click "Load Temporary Add-on"
5. Navigate to the LinguaFox directory and select the `manifest.json` file
6. The extension icon will appear in your Firefox toolbar

**Note:** For permanent installation, you would need to package the extension and submit it to Mozilla Add-ons, or install it as a developer extension.

## Setup

Before using LinguaFox, you need to configure your OpenAI API key:

1. Click the LinguaFox icon in your Firefox toolbar
2. Click the "Settings" button
3. Enter your OpenAI API key (get one from [OpenAI's platform](https://platform.openai.com/))
4. Optionally customize the system prompt
5. Click "Save Settings"

## Usage

1. Click the LinguaFox icon in your Firefox toolbar
2. Enter or paste the text you want to translate in the input field
3. Click "Translate"
4. The translated text will appear in the output field

## Files Structure

```
LinguaFox/
├── manifest.json      # Extension configuration
├── popup.html         # Main extension popup interface
├── popup.js           # Main functionality script
├── options.html       # Settings page
├── options.js         # Settings functionality
├── styles.css         # Styling for both popup and options
├── icons/             # Extension icons
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
└── README.md          # This file
```

## Note on Icons

The manifest.json file references icon files in the `icons` directory:
- `icons/icon16.png` (16x16 pixels)
- `icons/icon48.png` (48x48 pixels)
- `icons/icon128.png` (128x128 pixels)

You'll need to create these icon files or modify the manifest to use your own icons.

## Technical Details

- Uses OpenAI's GPT-4o model for high-quality translations
- Detects Chinese text using OpenAI API for accurate language detection
- Implements a clean, responsive UI with loading indicators
- Stores settings using Firefox's WebExtensions Storage API for persistence
- Compatible with Firefox's WebExtensions API (Manifest V2)

## Privacy

This extension:
- Stores your API key locally on your device
- Does not collect or transmit any data except to the OpenAI API for translation
- Does not track your browsing activity

## License

MIT License

## Support

For issues or feature requests, please create an issue in this repository.