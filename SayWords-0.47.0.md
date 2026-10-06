# SayWords 0.47.0

- **Background audio while you dictate.** Four choices in Settings → Dictation: leave it, lower it, pause it, or Smart. Lowering no longer changes the system volume. Pause stops what is playing (including a browser video) and resumes it afterwards; audio that cannot be paused is muted during the dictation. Smart classifies the sound on your Mac: speech is paused, music is only lowered. Needs the "System Audio Recording Only" permission.
- **Voices.** A new settings page: teach SayWords a person's voice from a short recording, design a new read-aloud voice from a text description, or clone a voice from a sample. Voice design and cloning use VoxCPM2 locally and need a separate install; the app shows the command.
- **Only my voice** (Soniox dictation). Speech from other people or from a video picked up by the microphone is left out of the text once you have recorded your own voice.
- **Speaker names in live captions** (Soniox). Each speaker starts a new line; people you added appear by name.
- Enter finishes a dictation, pastes and sends; Esc copies the text. The capsule closes by itself if nobody speaks.
- Redesigned settings window with previews.
- Fixes: the first words of a dictation are no longer lost; the local AI model starts only when needed and frees about 5 GB when idle; clock times are no longer replaced by emoji in the capsule.

**App identity changed.** SayWords now uses the identifier `com.berkinavci.saywords`. Settings, history, vocabulary and the Soniox key are carried over on first launch. macOS treats it as a new app, so grant Microphone, Accessibility and Screen Recording again when asked.

Apple Silicon; macOS 14 or later. Intel is not included. Speaker recognition, speaker names and pausing browser video are new and have had limited real-world testing. Lucide, FluidAudio, WhisperKit and Sparkle license notices are bundled with the app.
