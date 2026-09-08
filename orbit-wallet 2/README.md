# Orbit demo wallet

An original, dependency-free wallet UI prototype. No connection to any blockchain, wallet provider, payment service, or market-data API.

## Run

Open `index.html` in a modern browser. No installation or build is needed. Keep all three application files in the same folder.

For a consistent localStorage origin, optionally serve the folder:

```sh
cd orbit-wallet
python3 -m http.server 4173
```

Then open http://localhost:4173. This is only a static file server; the app needs no backend. Browser storage is separate for file URLs and each server origin.

## Files

- `index.html` — application shell
- `styles.css` — responsive design and animations
- `app.js` — views, settings, demo interactions, local persistence

## Customize

Open Settings from the top gear, account menu, or bottom navigation. Fields autosave to `orbit-demo-v1` in localStorage. Edit account details, total balance, daily changes, token details, and transaction records. Changing quantity or price calculates that token's value; its value can also be overridden. Total portfolio balance remains independently editable; use “Set balance to asset total” to synchronize it.

Transactions can be added, edited, or removed. Reset restores the original sample data after confirmation. All data is fictional; token prices and chart are illustrative, not current market information. Time controls select illustrative chart presentations, while the headline change stays daily. Collectibles intentionally has an empty state.

Receive displays a non-scannable QR-style placeholder and editable demo address. Send, Buy, and Swap display simulated previews and never alter holdings or submit transactions. No secrets, seed phrases, private keys, network requests, or real transaction signing are used.

## Verification

Checked in headless Chrome at 390 × 844 and desktop 1280 × 1000. Mobile horizontal overflow, localStorage reload persistence, receive dialog, swap preview, activity rows, search filtering, and runtime errors were checked. JavaScript syntax validation passed. There is no build step or dependency bundle.
