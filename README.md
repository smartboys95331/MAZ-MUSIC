# Building the Vynl APK online (no Android Studio, no downloads)

This folder is a ready-to-go Capacitor Android project with a GitHub Actions
workflow already included. GitHub's free servers will do the actual build —
you never install anything.

## Steps

1. Go to https://github.com and create a free account if you don't have one.
2. Click the **+** in the top right → **New repository**. Name it anything
   (e.g. `vynl-app`). Keep it **Public** (Actions minutes are unlimited and
   free for public repos) or Private (also free, just has a monthly minutes
   cap that's more than enough for occasional builds). Don't add a README —
   just click **Create repository**.
3. On the empty repo page, click **uploading an existing file**.
4. Drag this entire folder's contents into the upload box — both the
   `android` folder and the `.github` folder need to land at the top level
   of the repo. (Most browsers let you drag folders directly; if yours
   doesn't, zip the contents and GitHub will offer to unzip on upload — or
   use GitHub Desktop, which is free and simpler than dealing with Android
   Studio.)
5. Scroll down, click **Commit changes**.
6. Click the **Actions** tab at the top of your repo. You'll see "Build
   Vynl APK" running (a yellow dot). Wait 3–5 minutes for it to finish (green
   checkmark).
7. Click on the finished run, scroll to **Artifacts** at the bottom, and
   click **vynl-debug-apk** to download a zip containing your real
   `app-debug.apk`.
8. Transfer that APK to your Android phone and install it (you'll need to
   allow "install from unknown sources" the first time).

## Making changes later

If I send you an updated `index.html`, replace the file at
`android/app/src/main/assets/public/index.html` in your GitHub repo (GitHub
lets you edit/replace files directly in the browser — click the file, then
the pencil icon), commit the change, and the Actions workflow will
automatically rebuild a fresh APK for you.
