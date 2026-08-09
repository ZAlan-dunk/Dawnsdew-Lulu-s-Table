## Updates

- Fixed Android system Back navigation so in-app pages return to the previous surface.
- Added a two-step Home exit flow: first Back shows a hint, second Back opens an exit confirmation.
- Kept the Android version at `versionCode 12` / `versionName 0.6.5-Bata` and prepared an independent release signature for this named app copy.

## Functions

- Preserves recipe, pantry, specials, shopping list, and form navigation state while moving backward.
- Keeps the same recipe, pantry, specials, shopping-list, and navigation behavior as the source app; this independent package is not intended to cover-install the source app.

## Verification

- GitHub Actions run `31322516706` passed catalog validation, unit tests, Debug/Release Lint, Debug/Release assembly, and release signing verification. The release APK SHA-256 is `1365d11feab1f883f0d77124652a1184d2bb22f9b26412c0681ba9b86b386ff3`; no debug APK was published.
