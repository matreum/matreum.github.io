# matreum.github.io

Organization-level GitHub Pages root for the `matreum` GitHub organization. Currently serves:

- A minimal `index.html` placeholder at the root
- `.well-known/apple-app-site-association` — the AASA file establishing Universal Link ownership for the **Vanguard Validator** iOS app (`com.archer.OakleyValidator`). Used by the Meta Wearables Device Access Toolkit's auth callback flow.

## Updating the AASA file

The AASA file currently has a placeholder Team ID (`XXXXXXXXXX`). Before the iOS app's Universal Link routing can verify against Apple's content delivery network, replace the placeholder with the real 10-character Apple Developer Team ID — get it from Xcode → Settings → Accounts → click your Apple ID's team.

The AASA file **must not have a `.json` extension** and **must be served from the path** `/.well-known/apple-app-site-association` at the root of the domain (not under any subpath). Both invariants are enforced by Apple's fetcher.
