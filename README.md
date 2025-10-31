# Deep Learning Video-to-Text Summarizer

This project is a Python-based application that automatically generates a concise text summary from a video file. It leverages a sophisticated pipeline of deep learning models to understand both the visual and audio content of the video.

## Features

- **Audio Transcription**: Extracts audio from the video and uses OpenAI's Whisper to generate a full, accurate transcript.

- **Keyframe Analysis**: Intelligently selects unique visual frames to avoid redundant processing.

- **Image Captioning**: Generates descriptive text for each keyframe using a Vision-Language model (e.g., Salesforce BLIP).

- **Abstractive Summarization**: Combines the audio transcript and visual descriptions, then uses a Large Language Model (e.g., BART) to generate a fluent, human-like summary.

## How It Works

The system follows a multi-stage pipeline to process the video:

`Video Input` -> `Step A: Pre-processing` -> `Step B & C (Parallel)` -> `Step D: Aggregation` -> `Step E: Summarization` -> `Text Output`

1. Pre-processing: The video is split into its audio and visual frame components.

2. Audio Analysis: The audio is transcribed into text.

3. Visual Analysis: Unique keyframes are identified, and a text description is generated for each.

4. Aggregation: The audio and visual text streams are merged into a single chronological document.

5. Summarization: The final, coherent text summary is generated from the aggregated document.

## Technology Stack

- **Programming Language**: Python 3.8+
- **Deep Learning Frameworks**: PyTorch
- **Core Models & Libraries**:
    - Hugging Face transformers
    - OpenAI whisper for speech-to-text.
    - timm (PyTorch Image Models) for ResNet.
    - Salesforce BLIP for image captioning.
    - Facebook BART for summarization.
- **Video/Audio Tools**:
  - opencv-python
  - moviepy

## Setup and Installation
### Prerequisites:
- Python 3.8 or newer
- pip and venv
- ffmpeg (MoviePy dependency). You may need to install this separately using a package manager like Homebrew, Chocolatey, or apt.
- A GPU is highly recommended for reasonable performance.

Installation Steps:

Clone the repository:

git clone [https://github.com/your-username/video-summarizer.git](https://github.com/your-username/video-summarizer.git)
cd video-summarizer


Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`


Install the required Python packages:

pip install torch transformers opencv-python moviepy openai-whisper timm


Note: Ensure you install the correct version of PyTorch for your system (CPU or specific CUDA version).

How to Run

Place your video file (e.g., my_video.mp4) in the project's root directory.

Run the main script from your terminal:

python summarize.py --video_path my_video.mp4


The script will process the video and print the final summary to the console.

License

This project is licensed under the MIT License.