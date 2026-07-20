# Spotlight Publication Profile Helper

This app is a single-file browser tool. No `npm install`, build step, or local server is required.

## Open the app

1. Download or copy `index.html` to your computer.
2. Double-click `index.html` to open it in your browser.
3. If your browser blocks CDN scripts when opening local files, run any simple static server from this folder instead, for example:

   ```bash
   python3 -m http.server 4173
   ```

   Then open <http://127.0.0.1:4173/index.html>.

## Create and download an Excel file

1. Open `index.html` in your browser.
2. Add rows manually with **Add Row**, or import one or more `.xlsx` files with the upload area.
3. Fill or edit the publication profile fields in the table.
4. Click **Download .xlsx** in the bottom-right footer bar.
5. Your browser downloads a generated publication profile workbook.

## Downloaded file name

The app names the exported file from the first row when possible:

- `PublicationProfile_{group}_KW{week}.xlsx` when `group` and `validFrom` are filled.
- `PublicationProfile_{title/publisherName/fulfillmentCampaign}.xlsx` as a fallback.
- `PublicationProfile.xlsx` if no identifying fields are filled.

## Local data

Presets and column settings are stored locally in your browser using IndexedDB/local storage fallback. To move presets to another browser or device, use **Export Presets** and **Import Presets** inside the app.
