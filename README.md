# Mark As Done Extension for Online Courses

## Overview
The Mark As Done Extension is a browser extension designed to automate the process of marking tasks or assignments as completed on online college course platforms. With a single click, users can save time and effort by automatically clicking the "Mark as Done" button.

## Features
- **One-Click Automation**: Marks all pending tasks as completed instantly.
- **Simple & User-Friendly**: Easy-to-use interface for seamless interaction.
- **Customizable Selectors**: Adaptable to different online course platforms.
- **Lightweight & Efficient**: Minimal codebase ensures fast performance.

## How It Works
### Platform-Specific Selectors
The extension detects "Mark as Done" buttons on the webpage using JavaScript selectors.

### Automated Clicks
Once activated, the extension automatically clicks all identified buttons, marking tasks as done.

## Installation
### Manual Installation for Development
1. Clone or download this repository:
   ```sh
   git clone https://github.com/janvi-c16/Auto-Mark.git
   ```
2. Open your browser's extension management page:
   - **Chrome**: `chrome://extensions/`
   - **Edge**: `edge://extensions/`
3. Enable **Developer Mode**.
4. Click **Load unpacked** and select the folder containing the extension.

## Usage
1. Navigate to your online course platform.
2. Click the extension icon in the browser toolbar.
3. The extension will identify and automatically click all "Mark as Done" buttons.

## Key Files
- **manifest.json**: Defines extension metadata and permissions.
- **popup.html**: UI for the extension popup.
- **popup.js**: Contains JavaScript logic for automation.
- **content.js**: Handles interactions with the webpage DOM.

## JavaScript Logic Example
Here’s a simplified version of how the extension works:
```js
// Find all "Mark as Done" buttons
document.querySelectorAll('.mark-as-done-class').forEach((button) => {
    button.click();
});
alert("All tasks have been marked as done!");
```

## Customization
To make the extension work for a specific platform:
- Update the selector in `content.js` to match the platform’s "Mark as Done" button.
- Test and refine the logic as needed.

## Limitations
- Works only on platforms where buttons can be consistently identified.
- May require minor adjustments for different course platforms.

## Future Enhancements
- Support for multiple course platforms.
- Progress tracker showing completed tasks.
- Settings panel for easy customization without modifying code.

