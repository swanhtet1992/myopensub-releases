# MyOpenSub

MyOpenSub is a free desktop app that translates the subtitles a video already has, using AI, and burns the translation into the video or saves it as a subtitle file.

![The MyOpenSub editor: the list of videos, the video with its translated subtitles, and the original and translated lines side by side](editor.png)

## Download

**[Download the latest release](https://github.com/swanhtet1992/myopensub-releases/releases/latest)**, then choose the one file for your computer. In each file name, `…` is the version number.

| Your computer | File |
|---|---|
| Windows (64-bit) | `MyOpenSub-…-windows-x64-setup.exe` |
| Mac with Apple silicon (M1 or later), macOS 14 or later | `MyOpenSub-…-macos-apple-silicon.dmg` |
| Linux (64-bit): Debian, Ubuntu and other Debian-based systems | `MyOpenSub-…-linux-x64.deb` |
| Other Linux (64-bit) | `MyOpenSub-…-linux-x64.AppImage` (needs FFmpeg installed) |

There is no version for Macs with an Intel processor.

MyOpenSub uses FFmpeg, a free program, to read and encode video. The Windows and Mac files include it. The Linux files do not:

- The `.deb` installs FFmpeg with it when you install it the usual way: open it with your system's software installer, or run `sudo apt install ./MyOpenSub-…-linux-x64.deb` with the version number in place of `…`.
- For the AppImage, install FFmpeg first, with `sudo apt install ffmpeg` or your distribution's own ffmpeg package. Without it, MyOpenSub opens on a screen that says FFmpeg is needed.

Each release also holds `SHA256SUMS.txt`, for checking that a download arrived complete and unchanged, and `THIRD-PARTY-NOTICES.md` (see [Licences](#licences)). You do not need either to install MyOpenSub.

## First launch

This release does not yet carry the developer signature that Windows and macOS look for, so both warn you the first time you open MyOpenSub. Here is what to do on each system.

### Windows

TO CONFIRM: written after a tester's first launch.

### macOS

TO CONFIRM: written after a tester's first launch.

### Linux

TO CONFIRM: written after a tester's first launch.

## What you need

MyOpenSub is free. To translate, it needs your own API key for Gemini (from Google), Claude (from Anthropic) or OpenRouter: a code from that service that lets MyOpenSub translate on your account there. Open Settings with the button at the top right of the window (or press Ctrl+, on Windows and Linux, ⌘, on a Mac), choose the service under "Translate with", paste the key and click Save. The "Get a key from …" link under the box opens the page where you create one.

## What leaves your computer

Your videos never leave your computer.

**When you translate,** the subtitle text, and the Context and the names and terms from the Translate window, go to the service you chose, with your key. OpenRouter passes them on to the company behind the model you picked.

**When you export a translation** (burned into the video, or as a subtitle file), that episode's lines are sent to an open dataset of translations, so future models translate better:

| Sent | Never sent |
|---|---|
| Original and translated lines, with timing | Videos, audio, images |
| Which model wrote each line, and whether a person edited it | API keys |
| The names and terms, project name and video name | File locations, the Context you wrote, style, logo |
| The name you entered under "Credit as" in Settings, if any | Anything before an export: drafts stay on your computer |

**To turn this off,** switch off "Contribute this translation" in the Export window, or "Contribute exported translations" in Settings, under "Open dataset". Both are the same setting, and it is on by default.

**To delete what was sent,** open Settings and, under "Open dataset", next to "Already contributed", click "Delete from Dataset…", then "Delete". This deletes everything sent from this computer and turns contributing off.

## Problems

[Open an issue](https://github.com/swanhtet1992/myopensub-releases/issues/new/choose) here on GitHub (this needs a GitHub account). Say which version you have (it is at the bottom of Settings) and which system you use. Never paste an API key into an issue.

## Licences

Using MyOpenSub is covered by the [terms of use](TERMS.md). It includes software and fonts from other projects, which stay under their own licences. They are listed in `THIRD-PARTY-NOTICES.md`, attached to every [release](https://github.com/swanhtet1992/myopensub-releases/releases) and installed with the app.
