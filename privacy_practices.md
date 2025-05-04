# ChatGPT Timestamp – Privacy Practices

_Last updated: 05 May 2025_

## 1. Introduction  
**ChatGPT Timestamp** is an open-source Chrome extension that adds a local date-and-time label to every message in your ChatGPT conversations. We take privacy seriously and have designed the extension so that **all processing and storage happen entirely on your device**.

## 2. What data does the extension handle?

| Category              | Details                                                                 | Location                                | Retention                                               |
|-----------------------|-------------------------------------------------------------------------|-----------------------------------------|----------------------------------------------------------|
| **Message timestamps**| A single number (`Date.now()` in ms) for each ChatGPT message you see. | Stored with `chrome.storage.local`.     | Stays until you manually clear your browser’s extension data. |
| **Extension setting** | One boolean value `enabled` to remember if timestamps are hidden/shown.| Stored with `chrome.storage.local`.     | Same as above.                                           |

_No personal, behavioral, or sensitive data is ever collected or processed._

## 3. How is the data used?

- **Displaying timestamps:** When you revisit ChatGPT, the extension reads the saved timestamp for each message and shows it next to the message.
- **Remembering your toggle state:** The `enabled` flag preserves your visibility preference.

> **No data is synced, shared, sent to a server, or logged externally. Everything stays local.**

## 4. Permissions explained

| Permission                           | Why it's required                                                                  | Scope                       |
|-------------------------------------|-------------------------------------------------------------------------------------|-----------------------------|
| `storage`                           | To store and retrieve timestamps and the visibility toggle flag.                   | Local browser profile only. |
| `https://chat.openai.com/*`         | Allows the extension to access and modify ChatGPT's DOM to insert timestamps.      | Only ChatGPT pages.         |
| `https://chatgpt.com/*`             | Same as above.                                                                     | Only ChatGPT pages.         |
| `https://*.chatgpt.com/*`           | Ensures support for all current and future subdomains of ChatGPT.                  | Only ChatGPT pages.         |

The extension **does not** request permissions for `activeTab`, camera, microphone, notifications, or other sensitive APIs.

## 5. Remote code policy

All JavaScript is included in the extension package itself.  
✅ No remote scripts  
✅ No CDN libraries  
✅ No dynamic imports from external sources

## 6. Cookies and tracking

- ❌ No cookies  
- ❌ No fingerprinting  
- ❌ No analytics  
- ❌ No third-party trackers

## 7. Security measures

- Uses **Manifest V3**, which enforces a strict permission model and background isolation  
- Data is stored in `chrome.storage.local` and cannot be accessed by websites  

## 8. Children’s privacy

The extension is intended for general use and does **not** knowingly collect data from children under 13.

## 9. Changes to these practices

This document may be updated to reflect new features or legal requirements.  
The "Last updated" date at the top will always show the current version.  

## 10. Contact

For privacy questions or concerns, please contact:  
📧 **valmislab.studio@gmail.com**

---

_By using the ChatGPT Timestamp extension, you acknowledge that you have read and understood these Privacy Practices._
