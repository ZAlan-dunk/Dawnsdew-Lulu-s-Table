## Updates

- Fixed Android system Back navigation so in-app pages return to the previous surface.
- Added a two-step Home exit flow: first Back shows a hint, second Back opens an exit confirmation.
- Kept the Android version at `versionCode 12` / `versionName 0.6.5-Bata` and prepared an independent release signature for this named app copy.

## Functions

- Preserves recipe, pantry, specials, shopping list, and form navigation state while moving backward.
- Keeps the same recipe, pantry, specials, shopping-list, and navigation behavior as the source app; this independent package is not intended to cover-install the source app.

## Verification

- Back state tests, unit tests, Debug/Release Lint, Debug/Release assembly, APK metadata, signing, and upgrade identity checks are required before publication.
