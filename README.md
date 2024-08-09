# Witchcraft: Automagically Dubbing Videos with AI

Witchcraft is a local AI-based tool that automagically dubs videos into different languages. This project utilizes several others open source projects to make the process of extract audio, isolate voices, transcribe, translate, and generate audio, ensuring seamless synchronization with the original video while preserving background music.
The goal of this project is to empower users to perform the dubbing process on their own machines, eliminating the need to pay for various AI tools. By providing an accessible and free solution, Witchcraft aims to enhance the reach of knowledge through the translation of educational content and beyond.

# Steps to Automagically Dub Videos with AI

1. **Isolate Voice from Background Sound**  
   Use an audio separation tool to isolate the voice from the background sound, resulting in two separate files: `vocals.wav` and `accompaniment.wav`.

   **Tools:** [Spleeter](https://github.com/deezer/spleeter), [Demucs](https://github.com/facebookresearch/demucs)

2. **Transcription**  
   Transcribe the isolated voice (`vocals.wav`) into text (`transcription.txt`) using a transcription tool.

   **Tools:** [Vosk](https://github.com/alphacep/vosk), [Whisper](https://github.com/openai/whisper)

3. **Translate the Transcription**  
   Translate the transcribed text into the target language (`translated_transcription.txt`).

   **Tools:** [Helsinki-NLP/Opus-MT](https://github.com/Helsinki-NLP/Opus-MT), [Argos Translate](https://github.com/argosopentech/argos-translate)

4. **Text-to-Speech (TTS)**  
   Generate new audio from the translated transcription using TTS (`translated_audio.wav` or `translated_audio.mp3`).

   **Tools:** [Coqui TTS](https://github.com/coqui-ai/TTS), [Mozilla TTS](https://github.com/mozilla/TTS)

5. **Synchronize the Voice with the Video**  
   Align the newly generated audio with the correct timings in the video, ensuring proper synchronization (`synced_audio.wav` or `synced_audio.mp3`).

   **Tools:** [Aeneas](https://github.com/readbeyond/aeneas)

6. **Combine New Voice with Background Sound**  
   Mix the synchronized voice with the original background sound to create a single audio file (`final_audio.wav` or `final_audio.mp3`).

   **Tools:** [FFmpeg](https://ffmpeg.org/)

7. **Replace Original Audio with Generated Audio**  
   Replace the original audio in the video with the newly generated and mixed audio, keeping the video content intact (`final_video.mp4`).

   **Tools:** [FFmpeg](https://ffmpeg.org/)


