# SesCam

Dictation and live captions for Apple Silicon Macs.

SesCam lets you speak into your Mac and insert the result into another app. It
also offers live captions for system audio, on-device speech engines, optional
AI text cleanup, and app-specific writing rules.

## Beta status

[Download SesCam 0.30.2 beta 1](https://github.com/berkinefeavci/sescam/releases/tag/v0.30.2-beta.1) for Apple Silicon Macs running macOS 26 or later. The signed and notarized package was exercised on macOS 27.0.1; other Macs and macOS versions are untested.

This is a testing build. Microphone capture, global shortcuts, insertion into other apps, and live captions still need end-to-end reports from tester Macs. Start with short, non-sensitive speech and [report problems](https://github.com/berkinefeavci/sescam/issues).

## Install

1. Download the DMG from the [beta release](https://github.com/berkinefeavci/sescam/releases/tag/v0.30.2-beta.1) and drag SesCam to Applications.
2. Open Settings → Models and choose a speech engine. Apple or Whisper may download a local model.
3. Allow Microphone for dictation. Allow Accessibility only for inserting text into other apps. Live captions need Screen Recording permission for system audio.

There is no automatic updater in this beta; install future builds manually.

The source code is private during this beta. This repository is the public
product page and a place to report issues.

## Choose where speech is processed

- Apple speech and Whisper run on your Mac. Speech models may need a download.
- Soniox streams audio to Soniox and needs your own API key; provider charges
  may apply.
- AI text cleanup is optional. It can use a configured cloud provider or a
  local model. Screen context is off by default.

SesCam stores completed dictations in a local history file and shows the last
24 hours. Read [data use](PRIVACY.md) before testing with sensitive content.

## Feedback

Use [Issues](https://github.com/berkinefeavci/sescam/issues) for bugs and feature
requests. Include your Mac model, macOS version, selected speech engine, target
app, and steps to reproduce. Do not post API keys, private audio, transcripts,
or screenshots containing sensitive content.

---

Türkçe: SesCam, Mac için dikte ve canlı altyazı uygulamasıdır. [0.30.2 beta sürümü indirilebilir](https://github.com/berkinefeavci/sescam/releases/tag/v0.30.2-beta.1). Mikrofon, genel kısayol, başka uygulamaya yapıştırma ve canlı altyazı farklı Mac'lerde hâlâ test ediliyor. Apple ve Whisper cihazda çalışır; Soniox seçilirse ses Soniox'a gönderilir.
