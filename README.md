# Alphade

Remove semi-transparent watermarks, logos and text overlays from your own videos, on your Mac. Alphade brings back the picture underneath instead of blurring it away.

English | [繁體中文](README-zh_TW.md)

![Alphade comparing the original and the processed video](images/compare.png)

## What it does

Draw a box around the overlay. Alphade studies the whole video, works out how the overlay was blended in, and reverses it in every frame. Where an overlay is fully opaque on a simple background, it fills the area in smoothly from its surroundings instead.

- **Restores, not blurs**: a semi-transparent watermark is taken out of the picture, so what was underneath shows again.
- **Tells you before you export**: after the analysis, Alphade says whether the watermark removes cleanly, removes by filling in from the background, or will leave a blurry patch.
- **Check every frame**: step through the result, compare it with the original side by side, and play it from any moment.
- **Only the box changes**: export at the original size or downscale to 1080p or 720p, in H.264 or HEVC. The audio is copied as is.
- **Private**: everything runs on your Mac. Videos are never uploaded, there is no account, Alphade makes no network connections and collects no data.
- **Free**.

## Install

Requires macOS 26 or later. Tested on Apple silicon. Alphade is signed with a Developer ID and notarized by Apple.

### Download

1. Download `Alphade-<version>.zip` from [Releases](../../releases/latest).
2. Open the zip and drag **Alphade** to your Applications folder.
3. Open Alphade. macOS asks whether to open an app downloaded from the internet; click **Open**.

To uninstall, drag Alphade to the Trash. Its settings and temporary files are in `~/Library/Containers/app.vulcanshen.alphade`, which you can delete too.

### Homebrew

```sh
brew install --cask vulcanshen/tap/alphade
```

Update with `brew upgrade --cask alphade`. Uninstall with `brew uninstall --cask alphade`, or add `--zap` to delete its settings and temporary files too.

## Quick start

1. Click **Choose Video…** (or drop a video into the window).
2. Drag a box around the watermark, with a little room on every side.
3. Click **Analyze**.
4. Check the result with **Original**, **Processed** and **Compare**.
5. Click **Export…** and choose where to save. The name is filled in as `<original name>_nowm.mp4`.

## Keyboard

| Keys | Action |
|---|---|
| ⌘O | Open a video |
| ⌘E | Export |
| ⌘1 / ⌘2 / ⌘3 | Original / Processed / Compare |
| ← / → | Previous / next frame |
| Space | Play or pause (muted) |
| Hold O | Show the original while held |
| ⌘+ / ⌘− | Zoom in / out (after drawing the box) |
| ⌘, | Settings (language) |

## Works best with

- Semi-transparent watermarks, logos and text that stay in the same place throughout the video
- Opaque logos over simple backgrounds such as solid colors, gradients and slides
- 8-bit (SDR) MP4, MOV and M4V videos

## Not supported

- Watermarks that move or change position
- Opaque watermarks over detailed or live-action backgrounds (the area comes out blurry)
- 10-bit and HDR videos

## Use it on your own videos

Only edit videos you own or have permission to change. Removing someone else's watermark may break copyright law where you live, and you are responsible for how you use Alphade.

## Feedback

Report problems and ideas in [Issues](../../issues). The source code is not public.

## License

Alphade is free to download and use. © 2026 Vulcan Shen. All rights reserved. Alphade is provided "as is", without warranty of any kind.
