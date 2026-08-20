# ARC — The Journey (sealed)

`index.html` is a single, self-contained, **AES-256-GCM encrypted** presentation.
Without the passphrase it is unreadable — even fetched directly from its public URL.
Enter the passphrase and it plays itself: narrated, offline, no server, no tracking.

## Change passphrase or content
Plaintext source (art, audio, `scenes.js`) is kept privately outside this repo, in
`../masters/website-plaintext/` — never commit it here.
Rebuild with a new passphrase:
```
node ../masters/build-scripts/build_encrypted.js "your-new-passphrase"
# then copy the produced index.html over this one, commit, push
```

## Deploy
GitHub Pages (branch `main`, root) serves `index.html` directly.
Also runs from IPFS or any static host — the file needs nothing else.
