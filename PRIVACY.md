# SesCam beta: data use

SesCam is a macOS dictation and live caption app. This document describes the
current beta's behavior. Choose a speech engine and AI settings before using it
with sensitive content.

## Audio and text

- Apple speech and Whisper process speech on your Mac. Their speech models may
  be downloaded when selected.
- Soniox dictation streams recorded audio and configured vocabulary to Soniox.
  Soniox read-aloud sends the text you ask it to speak to Soniox. Soniox requires
  your own API key and may charge you under its terms.
- AI text editing sends the transcript and the project context you selected to
  the configured AI provider. If you select a local model, the request goes to
  that local service. Mini AI uses the separately configured Hermes connection.
- Screen context is off by default. If enabled, SesCam captures the selected
  target window for an AI request and removes its temporary capture afterward.

## Storage and permissions

- Completed dictations are saved in a local history file under Application
  Support. The app shows records from the last 24 hours, up to 200 entries.
  Older records are removed from that file when SesCam starts, history is
  opened, or a new dictation is saved. The file is not continuously purged
  while the app stays open. Avoid sensitive dictation in this beta if that
  retention does not suit you.
- API keys are stored in macOS Keychain. Settings and project vocabulary are
  stored on the Mac. A chosen Whisper model is stored under SesCam's Application
  Support folder.
- Microphone permission is used for dictation. Accessibility is used to insert
  text into other apps. Screen Recording is used for system audio captions and
  optional AI window context. Apple Events is used to read a browser tab's
  address for destination-specific formatting; that address is not sent by
  SesCam to an AI provider for that purpose.

Third-party providers process data under their own terms. SesCam does not have
an automatic updater in this beta.
