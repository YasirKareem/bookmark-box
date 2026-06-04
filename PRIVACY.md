# Privacy Policy — Bookmark Box

**Last updated: June 2026**

---

## Summary

Bookmark Box does not collect, transmit, or share any of your data.
Everything the extension stores stays on your device.

---

## What is stored and where

| Data | Storage location | Leaves your device? |
|---|---|---|
| Bookmark metadata (titles, URLs, tags, notes, folders) | `browser.storage.local` | No |
| Preview thumbnails (screenshots of saved pages) | IndexedDB in your browser profile | No |
| App settings and preferences | `browser.storage.local` | No |
| Capture queue state (for pause/resume across restarts) | `browser.storage.local` | No |

Data is only exported when you explicitly use the Export feature, and only to a file on your own device.

---

## What is not collected

- No usage analytics
- No crash reporting
- No telemetry
- No personal identifiers
- No browsing history beyond pages you explicitly save as bookmarks
- No communication with any remote server operated by this extension

---

## Permissions explained

### Required at install

**`bookmarks`**
Read and write access to your Firefox bookmarks. Without this permission, the extension cannot show, save, or manage your bookmarks.

**`storage`**
Saves app state, settings, tag data, and thumbnail metadata in `browser.storage.local`. All data remains on your device.

**`tabs`**
Reads the active tab's URL and title when you click Save, and accesses tab content for screenshot capture. The extension does not record or log your tab history.

**`clipboardWrite`**
Copies a bookmark URL to your clipboard when you use the Copy button. The extension does not read clipboard content.

**`downloads`**
Writes your exported backup file to your Downloads folder when you use Export. Nothing is uploaded.

---

### Optional — requested only when you activate a specific feature

**`<all_urls>`**

This permission is not granted at install. Firefox will ask you separately if you activate one of these features:

- **Preview Capture** — to take a screenshot of a bookmarked page, the extension must be able to visit that URL
- **Broken-Link Check** — to verify whether a saved URL is still reachable, the extension must be able to make a network request to it

No page content is retained beyond the screenshot thumbnail image. URLs visited during a broken-link scan are not logged, stored beyond the scan result, or transmitted anywhere.

You can decline this permission and the rest of the extension continues to work normally.

**`nativeMessaging`**

Not active in the standard release. Listed as optional for a possible future companion component. Granting this permission has no effect unless a separately installed native application is present on your system and explicitly configured.

---

## Data export

When you use the Export feature, Bookmark Box writes a JSON file to your Downloads folder. This file contains your bookmark metadata, tags, notes, and folder structure. It does not include screenshot thumbnails.

You control this file entirely. The extension does not upload it anywhere.

---

## Data deletion

To remove all data stored by Bookmark Box:

1. Remove the extension from Firefox via `about:addons`
2. Firefox automatically clears `browser.storage.local` entries for the extension on uninstall
3. IndexedDB data (thumbnails) is also cleared by Firefox when the extension is removed

---

## Contact

For questions about privacy, open an issue in this repository or contact:

hallo@yasirkareem.com
