# FontView Updates

Public distribution repository for FontView direct APK releases.

- `latest.json` is the public update manifest read by the Android app.
- APK binaries are published as GitHub Release assets (not committed to Git).
- The source code and signing configuration belong in the private `FontView` repository.

## Important

The current manifest is a placeholder for version 1.0.0. The all-zero SHA-256 is deliberately invalid. **Do not distribute an APK or install this manifest until a real signed APK has been published and its actual SHA-256 replaces the placeholder.**

## Publishing

1. Build a release APK from the private source repository using the permanent release keystore.
2. Publish the APK as `FontView-vX.Y.Z.apk` in a GitHub Release tagged `vX.Y.Z`.
3. Calculate the exact APK SHA-256 and update `latest.json` with the version code, version name, APK release URL and hash.
4. Commit the new manifest to this repository's `main` branch.
5. Test update detection, download, signature verification and Android's installer confirmation on a device.

Never publish the signing keystore or its passwords here.
