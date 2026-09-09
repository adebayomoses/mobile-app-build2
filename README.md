# Inwebtify — Android app

A [Capacitor](https://capacitorjs.com/) WebView wrapper around
<https://inwebtify.com/>, generated and maintained by the Esipher WordPress
plugin. Don't edit these files by hand — change the app's settings under
**Esipher → Mobile App** in wp-admin and Esipher re-pushes them here.

## Builds

Every push runs **.github/workflows/build-app.yml**, which outputs one
artifact, `esipher-app`, containing:

| File | Use |
| --- | --- |
| `app-debug.apk` | Install directly on a device to test (enable "install unknown apps"). |
| `app-release.aab` | Signed with your keystore — upload to the Google Play Console. |

Grab it from the newest green run under the repo's **Actions** tab, or
via **Esipher → Mobile App → Download latest build**.

## Signing

`build-app.yml` signs the release bundle with a keystore Esipher
generated and stored as repo secrets (`ESIPHER_KEYSTORE_BASE64`,
`ESIPHER_KEYSTORE_PASSWORD`, `ESIPHER_KEY_ALIAS`). Keep them — Google Play
permanently binds your app to this key.

Repo: adebayomoses/mobile-app-build2