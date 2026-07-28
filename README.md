# Ghost Rack

Remove the mannequin or model from product photos, leaving the garment on a clean studio backdrop — ready for shop listings.

Everything runs client-side in your browser. Photos are sent directly from your browser to Google's Gemini API using your own API key; nothing passes through any other server.

## How it works

1. Paste a Gemini API key (get one free at [aistudio.google.com/apikey](https://aistudio.google.com/apikey)).
2. Optionally edit the instruction prompt sent with every photo.
3. Drop in JPG/PNG photos of mannequin or model shots.
4. Click **Process photos**. Each photo is sent to the `gemini-2.5-flash-image` model and comes back with the mannequin/model removed, displayed as a before/after tile with a download link.

## Privacy

- The API key is held only in the page's memory (a plain input field) — it is never persisted to storage or sent anywhere except Google's Gemini API.
- Photos are processed one at a time in your browser tab and are not uploaded to any server other than Google's.

## Running locally

This is a single static HTML file with no build step or dependencies. Open `index.html` directly in a browser, or serve it:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
