NSV Pogo iPhone PWA
===================

This package is a Progressive Web App (PWA) version of the NSV Pogo standalone HTML app.

Files:
- index.html               Main app
- manifest.webmanifest     Home Screen / PWA metadata
- sw.js                    Offline cache service worker
- icons/                   iPhone / PWA icons

IMPORTANT
The PWA features (Home Screen standalone mode + reliable offline caching) require the files to be served from HTTPS, such as GitHub Pages. Opening index.html directly from the iPhone Files app does not provide full PWA behavior.

GITHUB PAGES QUICK SETUP
1. Create a GitHub repository, for example: nsv-pogo
2. Upload ALL files and folders from this package. Keep index.html, manifest.webmanifest and sw.js at the repository root, and keep the icons folder.
3. In GitHub: Settings > Pages.
4. Under Build and deployment choose: Deploy from a branch.
5. Choose branch: main and folder: / (root), then Save.
6. Wait for GitHub to show the published HTTPS address.
7. On iPhone, open the published address in Safari.
8. Tap Share > Add to Home Screen. If "Open as Web App" is shown, leave it enabled.
9. Launch NSV Pogo once while online. The service worker caches the app.
10. After that, the app can work offline using its cached files and embedded pin data.

UPDATING THE APP
If you publish a newer version later, change the CACHE value in sw.js from nsv-pogo-v1 to nsv-pogo-v2 (then v3, etc.) so iPhone refreshes the cached app files.
