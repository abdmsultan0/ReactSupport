# ReactSupport (Aliucord plugin)

Settings (plugin settings button -> bottom sheet):
- **Add IDs** – user IDs to watch (one per line).
- **Set react time** – seconds to wait before reacting (also spaces reactions apart).
- **Start / Stop** – master switch.

When started: if a saved ID reacts to one of YOUR messages, the plugin reacts
to that same message with the same emoji (unicode or custom) after the delay.

## Build
Easiest: copy the `ReactSupport/` folder into the official
https://github.com/Aliucord/plugins-template (add `include(":ReactSupport")`
to its settings file), then run:

    ./gradlew ReactSupport:make

Copy `ReactSupport/build/outputs/ReactSupport.zip` to
`/storage/emulated/0/Aliucord/plugins/` on the phone and enable it.

## Build without a PC (GitHub Actions)
1. Create a free GitHub repo and upload everything in this folder (including `.github`).
2. Open the repo -> Actions -> "Build plugin" -> Run workflow.
3. When it finishes, download the `ReactSupport` artifact, unzip it once.
   Inside is `ReactSupport.zip` containing `classes.dex` + `manifest.json`
   (same format as your example). Put it in `Aliucord/plugins/`.
