# SayWords: data use

SayWords is a macOS dictation and live caption app. Choose a speech engine and
AI settings before using it with sensitive content.

## Audio and text

- Apple speech and Whisper process speech on your Mac. Their speech models may
  be downloaded when selected.
- Soniox dictation streams recorded audio and configured vocabulary to Soniox.
  Soniox read-aloud sends the text you ask it to speak to Soniox. Soniox requires
  your own API key and may charge you under its terms.
- AI text editing sends the transcript and the project context you selected to
  the configured AI provider. If you select a local model, the request goes to
  that local service. Mini AI uses the separately configured Hermes connection.
- Screen context is off by default. If enabled, SayWords captures the selected
  target window for an AI request and removes its temporary capture afterward.

## Storage and permissions

- Completed dictations are saved in a local history file under Application
  Support. The app shows records from the last 24 hours, up to 200 entries.
  Older records are removed from that file when SayWords starts, history is
  opened, or a new dictation is saved. The file is not continuously purged while
  the app stays open.
- API keys are stored in macOS Keychain. Settings and project vocabulary are
  stored on the Mac. A chosen Whisper model is stored under SayWords'
  Application Support folder.
- Microphone permission is used for dictation. Accessibility is used to insert
  text into other apps. Screen Recording is used for system audio captions and
  optional AI window context. Apple Events is used to read a browser tab's
  address for destination-specific formatting; that address is not sent by
  SayWords to an AI provider for that purpose.
- Automatic update checks are off by default. If enabled, they fetch an
  appcast from GitHub once a day. When you approve an update, SayWords downloads it from GitHub
  Releases and verifies its signature before installation.

- Vocabulary learning uses only dictation corrections and text you explicitly
  paste into the vocabulary screen. The pasted source text is not retained;
  proposed terms and corrections are stored locally. Accepted terms are sent
  as recognition hints when Soniox is selected. Automatic acceptance is off
  by default.

## Background audio, voices and speaker recognition

- When background audio is set to lower, pause or Smart, SayWords captures
  other apps' audio output during dictation in order to lower, mute or classify
  it. That audio is processed in memory on your Mac. It is not written to disk
  and is not sent anywhere. This uses the "System Audio Recording Only"
  permission. Pausing sends the system play/pause media key.
- Voice samples you record or import in Voices, and the voiceprints derived
  from them, are stored only under SayWords' Application Support folder.
  Voiceprints are computed on your Mac with a model downloaded once from
  Hugging Face. Deleting a person removes the sample and the voiceprint.
- "Only my voice" and speaker names in captions turn on Soniox speaker
  diarization for audio that is already being sent to Soniox. Matching a
  speaker to a saved person happens on your Mac; voiceprints are not uploaded.
- Voice design and cloning run locally with VoxCPM2 in a separate Python
  environment that you install. Text and reference audio are not sent to any
  service. The model is downloaded once from Hugging Face.
- A local diagnostic log (debug.log under Application Support) records
  background-audio and voice-filter decisions: timestamps and similarity
  scores, never audio or transcript text.

Third-party providers process data under their own terms.
