# Christmas DIY Advent

Installable phone app (PWA) on GitHub Pages, shared between two phones via Firebase Firestore.

## Setup (about 10 minutes)

1. **Firebase**: console.firebase.google.com → Add project (Analytics off).
   - Build → Firestore Database → Create database (production mode, region europe-west2).
   - Firestore → Rules → paste `firestore.rules` → Publish.
   - Project settings → Your apps → Web (`</>`) → register → copy the `firebaseConfig` values into `config.js`.
2. **GitHub**: new repo, push these files, Settings → Pages → Deploy from branch `main` / root.
3. **Phones**: open the Pages URL.
   - iPhone: Safari → Share → Add to Home Screen.
   - Android: Chrome → ⋮ → Add to Home screen / Install app.

The first phone to open it loads the starting tasks into Firestore; after that both phones share one calendar live.

Notes
- `CALENDAR_ID` in `config.js` is the only key to your list. Anyone with the site URL can read the code, so don't put anything private in tasks.
- `seed.js` is scrambled so the tasks don't spoil. Don't decode it.
- Works offline; changes sync when back online.
