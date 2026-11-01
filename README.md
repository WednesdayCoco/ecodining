# ANU EcoDining

A single-file low-carbon food choice prototype for the ANU HCI course, plus a ready-to-install Android APK.

## Files

- `index.html` — the complete PWA prototype
- `EcoDining.apk` — signed Android app, Android 7.0 and newer
- `.nojekyll` — makes GitHub Pages serve the folder as plain static files

## 1. Deploy the fixed GitHub Pages link

### Option A — GitHub website

1. Create a new **public** repository at https://github.com/new. Name it `ecodining`.
2. In the repository, choose **Add file → Upload files**.
3. Upload `index.html`, `EcoDining.apk`, `.nojekyll`, and this `README.md` to the repository root.
4. Commit the files.
5. Open **Settings → Pages**.
6. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
7. Select branch **main** and folder **/ (root)**, then save.
8. Wait for the Pages deployment to finish. The fixed app link will be:

   `https://YOUR-GITHUB-USERNAME.github.io/ecodining/`

   The APK link will be:

   `https://YOUR-GITHUB-USERNAME.github.io/ecodining/EcoDining.apk`

### Option B — Git command line

Run these commands from this folder, replacing the placeholders:

```bash
cd D:\8280\ecodining-site
git init
git add .
git commit -m "Add ANU EcoDining PWA and Android APK"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/ecodining.git
git push -u origin main
```

Then enable **Settings → Pages → Deploy from a branch → main → / (root)**.

GitHub Pages needs a public repository on the free plan. Activating Pages can take one or two minutes.

## 2. Install the APK on Android

1. Open `https://YOUR-GITHUB-USERNAME.github.io/ecodining/EcoDining.apk` in Chrome on the phone.
2. If Chrome warns about downloading an APK, choose **Download anyway**.
3. Open the downloaded `EcoDining.apk` from Downloads or Files.
4. Allow **Install unknown apps** for Chrome/Files when Android asks.
5. Tap **Install**, then open **EcoDining** from the Home screen.

The APK is self-contained and bundles its JavaScript libraries. It does not need the website to run.

The APK is signed for direct installation. Keep the private signing keystore if you plan to publish future updates.
