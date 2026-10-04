# SayWords

Dictation and live captions for Apple Silicon Macs.

SayWords lets you speak into your Mac and insert the result into another app. It
also offers live captions for system audio, on-device speech engines, optional
AI text cleanup, and app-specific writing rules.

## Download

[Download SayWords](https://github.com/berkinefeavci/sescam/releases/latest) for Apple Silicon Macs. The package is signed and notarized. It has been exercised on macOS 27; other Macs and macOS versions are less tested, so start with short, non-sensitive speech and [report problems](https://github.com/berkinefeavci/sescam/issues).

SayWords was called SesCam until 0.40.0.

## Install

1. Download the DMG from the [latest release](https://github.com/berkinefeavci/sescam/releases/latest) and drag SayWords to Applications.
2. Open Settings → Models and choose a speech engine. Apple or Whisper may download a local model.
3. Allow Microphone for dictation. Allow Accessibility only for inserting text into other apps. Live captions need Screen Recording permission for system audio.

## Updates

Automatic update checks are off by default. You can enable daily checks in Settings, or choose “Check for Updates” manually. The update window downloads, verifies, and installs a release after you approve it. If you have the 0.30.2 beta (SesCam), install the latest version by hand once.

The source code is private for now. This repository is the public
product page and a place to report issues.

## Choose where speech is processed

- Apple speech and Whisper run on your Mac. Speech models may need a download.
- Soniox streams audio to Soniox and needs your own API key; provider charges
  may apply.
- AI text cleanup is optional. It can use a configured cloud provider or a
  local model. Screen context is off by default.

SayWords stores completed dictations in a local history file and shows the last
24 hours. Read [data use](PRIVACY.md) before testing with sensitive content.

## Feedback

Use [Issues](https://github.com/berkinefeavci/sescam/issues) for bugs and feature
requests. Include your Mac model, macOS version, selected speech engine, target
app, and steps to reproduce. Do not post API keys, private audio, transcripts,
or screenshots containing sensitive content.

---

Türkçe: SayWords (eski adı SesCam), Mac için dikte ve canlı altyazı uygulamasıdır. [Son sürümü indirin](https://github.com/berkinefeavci/sescam/releases/latest). Yeni sürüm çıkınca uygulama bildirir ve kendi içinden günceller. Apple ve Whisper cihazda çalışır; Soniox seçilirse ses Soniox'a gönderilir.
