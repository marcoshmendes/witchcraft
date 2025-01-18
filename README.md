# Witchcraft - AI-Powered Video Dubbing Tool 🌍🎥

**Witchcraft** is an open-source command-line tool that automates the process of dubbing videos into another language. Its primary goal is to expand knowledge by breaking down language barriers, enabling people around the world to access and understand educational content and online videos in their native language. 🌟

While we aim to incorporate as much open-source technology as possible, this tool leverages powerful APIs from industry leaders like OpenAI to ensure high-quality results. Open-source components are included wherever feasible. 💡

## Features ✨

- **YouTube Video Input**: Simply provide the URL of a YouTube video. 📹
- **Automatic Transcription**: Extract the speech from the video and generate a timestamped transcription. 📝
- **Translation**: Translate the transcription into the target language. 🌐
- **Text-to-Speech (TTS)**: Generate audio from the translated transcription. 🎙️
- **Synchronization**: Ensure the new audio aligns perfectly with the original video. 🔄
- **Seamless Output**: Replace the original audio track in the video with the newly generated dubbed audio. 🎧

## How It Works 🛠️

### Steps to Automagically Dub Videos with AI 🪄

1. **Transcription with Timestamps**
   - Extract speech from the video and generate a timestamped transcription.
   - **API Used**: OpenAI Whisper

2. **Translate the Transcription**
   - Translate the transcribed text into the target language.
   - **API Used**: OpenAI GPT models for high-quality translation 🌟

3. **Text-to-Speech (TTS)**
   - Generate new audio from the translated transcription.
   - **API Used**: OpenAI TTS (or other advanced TTS APIs for specific languages) 🎤

4. **Synchronize the Voice with the Video**
   - Align the newly generated audio with the video’s original timings to ensure proper synchronization.
   - **Tools**: FFmpeg for timing alignment and adjustments 🕒

5. **Replace Original Audio with Generated Audio**
   - Replace the original video’s audio with the newly generated and synchronized dubbed audio, keeping the video content intact.
   - **Tools**: FFmpeg 🎬

## Installation ⚙️

### Prerequisites

- **Node.js** (v16 or later) 🖥️
- **FFmpeg** (Ensure it’s installed and added to your system PATH) 🛠️
- API keys for the services you plan to use (e.g., OpenAI) 🔑

### Clone the Repository
```bash
$ git clone https://github.com/marcoshmendes/witchcraft.git
$ cd witchcraft
```

### Install Dependencies
```bash
$ npm install
```

### Set Up Environment Variables
Create a `.env` file in the project root and add your API keys:
```env
OPENAI_API_KEY=your_openai_api_key
```

## Usage 🚀

### Basic Command
Run the following command, providing the URL of the YouTube video you want to dub:
```bash
$ node index.js --url <youtube_video_url> --language <target_language_code>
```
- `--url`: The YouTube video URL. 🌐
- `--language`: The target language code (e.g., `en` for English, `es` for Spanish). 🗣️

### Example
```bash
$ node index.js --url https://www.youtube.com/watch?v=dQw4w9WgXcQ --language es
```
This will process the video, translate it into Spanish, and output the dubbed video with synchronized audio. 🎉

### Output
The output will be a video file with the new dubbed audio track:
```
output/final_video.mp4
```

## Contributing 🤝

Contributions are welcome! Feel free to open issues, submit pull requests, or suggest new features. For major changes, please open an issue first to discuss what you’d like to change. 💬

1. Fork the repository 🍴
2. Create your feature branch (`git checkout -b feature/AmazingFeature`) 🌟
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`) ✍️
4. Push to the branch (`git push origin feature/AmazingFeature`) 🚀
5. Open a pull request 🔄

## License 📜

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. ✅

## Roadmap 🗺️

- Support for additional video platforms (e.g., Vimeo, Dailymotion) 🌐
- Improve synchronization with machine learning models 🤖
- Add support for more languages and accents in TTS 🗣️
- Enhance error handling and user feedback 🛡️

## Acknowledgments 🙌

- **OpenAI Whisper** for transcription.
- **OpenAI GPT** for translation services.
- **OpenAI TTS** for text-to-speech.
- **FFmpeg** for video and audio processing.

We hope Witchcraft becomes a valuable tool for educators, creators, and anyone looking to expand knowledge by breaking down language barriers! 🌟

