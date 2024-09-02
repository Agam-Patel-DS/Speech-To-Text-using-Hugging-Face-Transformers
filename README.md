# Speech-to-Text with TensorFlow and Hugging Face Transformers

This project demonstrates how to perform speech-to-text (STT) transcription on `.m4a` audio files using TensorFlow, Hugging Face's Wav2Vec2 model, and Librosa for audio processing. The implementation resamples the audio to 16 kHz and converts it to mono before feeding it into a pre-trained Wav2Vec2 model to generate transcriptions.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project uses the Wav2Vec2 model from Hugging Face Transformers, which is a state-of-the-art model for automatic speech recognition (ASR). The code can process `.m4a` files and output a transcription of the audio. The core of the implementation relies on TensorFlow to run the Wav2Vec2 model, with Librosa handling audio resampling.

## Prerequisites

Before running the code, ensure you have the following:

- Python 3.7 or higher
- Basic understanding of Python and TensorFlow
- Familiarity with audio processing concepts

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://https://github.com/Agam-Patel-DS/Speech-To-Text-using-Hugging-Face-Transformers.git
   cd speech-to-text-tensorflow
   ```

2. **Install Required Python Packages**

   Install the necessary dependencies using `pip`:

   ```bash
   pip install tensorflow torchaudio librosa transformers
   ```

## Usage

To use this project to transcribe an `.m4a` audio file:

1. Place your `.m4a` audio file in the project directory.

2. Modify the `file_path` variable in the code to point to your audio file.

3. Run the script:

   ```bash
   python speech_to_text.py
   ```

4. The transcription will be printed to the console.

## Code Explanation

Here is a brief overview of the main components of the code:

- **load_audio(file_path)**: Loads the audio file and returns the waveform and sample rate.
- **preprocess_audio(waveform, sample_rate)**: Resamples the audio to 16 kHz, converts it to mono if necessary, and prepares it for model input.
- **speech_to_text(waveform)**: Uses the Wav2Vec2 model to generate the transcription from the preprocessed audio.
- **process_audio_file(file_path)**: Combines the above functions to load, preprocess, and transcribe the audio file.

### Example

Here's a sample code snippet showing how to transcribe an audio file:

```python
file_path = "your_audio_file.m4a"
transcription = process_audio_file(file_path)
print(f"Transcription: {transcription}")
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

## License

This project is licensed under the Apache 2.0 License.
