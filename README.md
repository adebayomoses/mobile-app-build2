# Afrirates - mobile app

A [Capacitor](https://capacitorjs.com/) WebView wrapper around
<https://afrirates.com/>, generated and maintained by the Esipher
plugin. Don't edit these files by hand - change the app's settings under
Esipher -> Mobile App in wp-admin and Esipher re-pushes them here.

## Builds

The bundled workflow (.github/workflows/build-app.yml) is run from the
plugin. It outputs an "esipher-app" artifact (app-debug.apk to sideload,
app-release.aab for the Google Play Console) and, when iOS is configured,
an "esipher-app-ios" artifact (App.ipa for App Store Connect).

Grab them from the newest green run under the repo's Actions tab, or via
Esipher -> Mobile App -> Download latest build.

## Signing

The workflow signs with keys Esipher generated and stored as repo
secrets. Keep them - the app stores permanently bind your app to them.

Repo: adebayomoses/mobile-app-build2
