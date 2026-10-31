# Krogoth: website and Android

## Website

GitHub Pages serves the same static `index.html` as the Android PWA. In repository Settings > Pages, select Deploy from a branch, `main`, `/ (root)` and Save. If Pages is unavailable for the private repository, use a hosting service that supports private repositories, or change repository visibility only if you want the source public.

## Android installation

Once the site is live on HTTPS, open its URL in Chrome on Android, open the three-dot menu and choose Install app (or Add to Home screen, depending on Chrome's installability check). This launches Krogoth separately from Claude. The manifest, icon and service worker provide installability and offline caching.

## Native APK

For a distributable APK, package the hosted PWA with Bubblewrap / Trusted Web Activity, configure Android signing and assetlinks.json verification for your hosting domain. An APK is not included in this branch.

## Updates

Changes merged into main will appear on the website after deployment; installed PWAs pick up updates when online. Check the deployed game on a phone before distribution.
