# SesCam

Dictation and live captions for Apple Silicon Macs.

SesCam lets you speak into your Mac and insert the result into another app. It
also offers live captions for system audio, on-device speech engines, optional
AI text cleanup, and app-specific writing rules.

## Beta status

A limited beta for macOS 26 or later is being prepared. **There is no public
download yet.** The current beta package has been signed and notarized, but
microphone, shortcut, paste, and captions behavior still needs live acceptance
on the Macs used by testers.

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

Türkçe: SesCam, Mac için dikte ve canlı altyazı uygulamasıdır. Sınırlı beta
hazırlanıyor; henüz herkese açık indirme bağlantısı yok. Apple ve Whisper
cihazda çalışır; Soniox kullanılırsa ses Soniox'a gönderilir.
