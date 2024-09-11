## Chrome Extension: Light Mode to Dark Mode Toggle

This Chrome extension allows users to switch between light mode and dark mode with a simple button. Below is an explanation of the different sections of the `manifest.json` file and their roles in the extension.

### 1. **Name**

- `"name": "Chrome Extension"`
  - **Explanation**: This field denotes the name of the Chrome extension, which will be visible to users when they install or interact with it.

### 2. **Description**

- `"description": "Go from light mode to dark mode and vice versa"`
  - **Explanation**: This field provides a short description of what the extension does. This is for users or developers to understand the extension's functionality at a glance.

### 3. **Version**

- `"version": "1.0.0"`
  - **Explanation**: This indicates the version of the extension. If any updates are made, this version number should be incremented accordingly. Typically, a major update (such as adding a new feature) would result in a version like "2.0.0."

### 4. **Manifest Version**

- `"manifest_version": 2`
  - **Explanation**: This specifies which version of the Chrome extension manifest your extension uses. Manifest version 2 is standard for Chrome extensions and outlines the structure of the manifest file.

### 5. **Background**

- `"background": { "scripts": ["popup.js"], "persistent": true }`
  - **Explanation**: The background section contains scripts that run behind the scenes in the extension, even when the popup or UI isn't visible.
    - `"scripts": ["popup.js"]`: This script contains the logic needed to toggle between light and dark modes.
    - `"persistent": true`: This means the background script stays active as long as Chrome is open. It ensures that the extension keeps working in the background.

### 6. **Browser Action**

- `"browser_action": { "default_file": "Appearance", "default_popup": "popup.html" }`
  - **Explanation**: The `browser_action` defines what happens when the user interacts with the extension's icon in the browser toolbar.
    - `"default_file": "Appearance"`: This specifies the label for the browser action button related to the extension’s functionality.
    - `"default_popup": "popup.html"`: This defines the popup UI that appears when the user clicks on the extension's icon. The popup file (`popup.html`) handles the user interface for toggling between light and dark modes.

### 7. **Permissions**

- `"permissions": ["https://*/*", "http://*/*", "tabs"]`
  - **Explanation**: Permissions specify what the extension is allowed to access. In this case:
    - `"https://*/*"` and `"http://*/*"`: The extension can interact with any secure (`https`) or non-secure (`http`) websites.
    - `"tabs"`: This allows the extension to access and modify the contents of browser tabs. For instance, it might apply the light or dark mode styles to all open tabs simultaneously.
