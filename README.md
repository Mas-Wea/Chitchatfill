# Chitchatfill – Auto expander

- Press `==` in any text area/contenteditable to open the picker.
- Type to search, use `↑/↓`, press `Enter` to expand.
- Click the toolbar icon to open the side panel to add/edit snippets, and Import/Export.
- Assign optional categories to snippets to keep them grouped and quickly filter both in the side panel and inline picker.

## Load
1. Visit `chrome://extensions`.
2. Enable **Developer mode**.
3. Click **Load unpacked** and pick this folder.

Snippets are stored in `chrome.storage.local` and can be exported/imported (AES‑GCM encrypted).

## TinyMCE (Rich Editor) – Self‑hosted
This build integrates TinyMCE into the **Custom snippet** modal.

**How to enable:**
1. Download **TinyMCE Community self‑hosted** zip from tinymce.com.
2. Copy the *contents* of the `tinymce/` folder into:
   `sidepanel/vendor/tinymce/`
   (replace the placeholder `tinymce.min.js` I added).
3. Reload the extension from `chrome://extensions` (Load unpacked).

**Notes**
- MV3 disallows remote scripts, so a CDN script will not work inside the side panel.
- If TinyMCE is not present, the UI gracefully falls back to the original editor.
- Saved rich content is stored as HTML (`snip.html`) and a plain‑text preview is derived for listing.

## Privacy & data use
- Snippets and settings are stored locally in chrome.storage.
- When you use AI paraphrase or AI assistant, your prompt text is sent to the OpenAI API using your own API key.
- When you use Submit Spreadsheet, the form data is sent to the Google Apps Script Web App URL you configure.
- See `PRIVACY.md` for details.
