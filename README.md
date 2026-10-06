# SayWords

Dictation and live captions for Apple Silicon Macs.

SayWords lets you speak into your Mac and insert the result into another app. It
also offers live captions for system audio, on-device speech engines, optional
AI text cleanup, app-specific writing rules, speaker recognition, and local
voice design and cloning for read-aloud.

## Download

[Download SayWords](https://github.com/berkinefeavci/saywords/releases/latest) for Apple Silicon Macs. The package is signed and notarized. It has been exercised on macOS 27; other Macs and macOS versions are less tested, so start with short, non-sensitive speech and [report problems](https://github.com/berkinefeavci/saywords/issues).

SayWords was called SesCam until 0.40.0. From 0.47 the app also uses a new
internal identifier (`com.berkinavci.saywords`). Your settings, history and API
key are carried over on first launch, but macOS treats it as a new app: grant
Microphone, Accessibility and Screen Recording again when asked.

## Install

1. Download the DMG from the [latest release](https://github.com/berkinefeavci/saywords/releases/latest) and drag SayWords to Applications.
2. Open Settings → Models and choose a speech engine. Apple or Whisper may download a local model.
3. Allow Microphone for dictation. Allow Accessibility only for inserting text into other apps. Live captions need Screen Recording permission for system audio. Lowering or pausing background audio during dictation needs the “System Audio Recording Only” permission.

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

## Background audio while you dictate

Settings → Dictation → background audio has four choices: leave it, lower it,
pause it, or Smart. Lowering does not change the system volume. Pause stops
whatever is playing (including a browser video) and resumes it afterwards;
audio that cannot be paused is muted for the length of the dictation. Smart
classifies what is playing on your Mac: speech is paused, music is only lowered.

## Voices and speaker recognition

- **People.** Record about 12 seconds of a voice in Settings → Voices. SayWords
  derives a voiceprint on your Mac.
- **Only my voice** (Soniox dictation): other people's speech and video audio
  picked up by the microphone are left out of the text. Mark your own recording
  as “This is me” first.
- **Speaker names in live captions** (Soniox): each speaker starts a new line;
  people you added appear by name.
- **Voice design and cloning** for read-aloud use VoxCPM2, which runs locally
  and is installed separately (the app shows the command). Describe a voice in
  words, listen to previews, and save the one you like, or clone a voice from a
  short recording. Requires Apple Silicon and several GB of disk space.

These features are new and have had limited real-world testing; speaker
recognition thresholds may need tuning for your microphone.

## Vocabulary and inline icons

The dictionary keeps manual words separate from learned suggestions. Suggestions
come from dictation corrections or text you explicitly paste into the dictionary;
automatic acceptance is off by default. Accepted terms can be sent to Soniox as
recognition hints when Soniox is selected.

Public builds use colorful Lucide icons for general words and keep brand names
as text. Inline art changes only the capsule display, never pasted text or history.
Lucide ISC and Feather MIT license notices are bundled with the app, together
with notices for FluidAudio, WhisperKit and Sparkle.

## Feedback

Use [Issues](https://github.com/berkinefeavci/saywords/issues) for bugs and feature
requests. Include your Mac model, macOS version, selected speech engine, target
app, and steps to reproduce. Do not post API keys, private audio, transcripts,
or screenshots containing sensitive content.

---

Türkçe: SayWords (eski adı SesCam), Mac için dikte ve canlı altyazı uygulamasıdır. [Son sürümü indirin](https://github.com/berkinefeavci/saywords/releases/latest). Güncellemeler elle denetlenebilir; günlük denetim Ayarlar’dan açılır. Onayınızla uygulama içinden kurulur. Apple ve Whisper cihazda çalışır; Soniox seçilirse ses Soniox'a gönderilir. 0.47 ile uygulama kimliği değişti: ayarlar taşınır, macOS izinleri yeniden verilir. Yeni: arka plan sesini kısma/durdurma/akıllı mod, kişileri sesinden tanıma, tarifle ses tasarlama ve ses kopyalama.
