Added the ability to modify item AWESOME Sink points and unlock Resource Scanning from schematics. (Thanks Mirrym, BlueBeka, and Th3Fanbus!)




****

<!-- _If you enjoy my work, please consider donating to my [completely optional tip jar](https://ko-fi.com/robb4)._ -->

## New Stuff

<!-- cspell:ignore BlueBeka Miirym -->
- Support for defining and patching the AWESOME Sink points of items (thanks Miirym and Th3Fanbus! [PR #28](https://github.com/Nogg-aholic/ContentLib/pull/28) [Docs PR#8](https://github.com/budak7273/ContentLib_Documentation/pull/8))
  - Specify a track via `ResourceSinkTrack`
  - Specify points via `ResourceSinkPoints` or make it unsinkable by setting it to `0`
  - Point values generally follow a predictable pattern. You can automatically calculate sensible values to use with [TFIT's developer tools](https://github.com/blockout22/TFIT#developer-utilities).
- Schematics can now unlock resources for scanning (thanks BlueBeka and Th3Fanbus! [PR #25](https://github.com/Nogg-aholic/ContentLib/pull/25) [Docs PR#7](https://github.com/budak7273/ContentLib_Documentation/pull/7))
  - Specify resource node types via `ScannableResources`
    - The JSON schema walks you through building these
  - Patches can clear previously defined resources via `ClearScannableResources`

## Changed Stuff

- Improved error logging for a few cases
- The JSON schemas have been extended with additional description information and error checking capabilities

## Fixed Stuff

- Fixed serialized recipe output (in logs and exports) still using the old `OverrideCategory` field name.
- VSCode now requires trusting JSON schema URLs before they can be used for validation.
  Directions on how to do this have been added to the [Setup page of the docs](https://docs.ficsit.app/contentlib/latest/Tutorials/Setup.html).

## Info for Developers

ContentLib relies on FindObject with the ANY_PACKAGE specifier
to implement the arbitrary class finding from string functionality.
ANY_PACKAGE is currently deprecated and a future update will change it to search the Asset Registry instead.
It is unknown if or how this will affect other mods using ContentLib's features.
The plan is to try and make the switch seamless.

## Known Bugs

See the [GitHub issues page](https://github.com/Nogg-aholic/ContentLib/issues?q=label%3Abug).
