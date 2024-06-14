# Audio Transcription and Meeting Minutes with OpenAI

This project transcribes audio files using OpenAI's Whisper model and generates meeting minutes including an abstract summary, key points, action items, and sentiment analysis using OpenAI's GPT-4 model.

## Features

- Transcribes audio files to text using OpenAI's Whisper model.
- Generates an abstract summary of the transcription.
- Extracts key points and action items from the transcription.
- Performs sentiment analysis on the transcription.
- Saves the generated meeting minutes to a DOCX file.

## Prerequisites

- Python 3.7+
- OpenAI API Key

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/audio-transcription-meeting-minutes.git
    cd audio-transcription-meeting-minutes
    ```

2. Create and activate a virtual environment:

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:

    ```bash
    pip install openai python-docx python-dotenv
    ```

4. Create a `.env` file in the root directory of the project and add your OpenAI API key:

    ```plaintext
    OPENAI_API_KEY=your_api_key_here
    ```

## Usage

1. Replace `your_api_key_here` with your actual OpenAI API key in the `.env` file.

2. Update the `audio_file_path` variable in the script to point to your audio file:

    ```python
    audio_file_path = "/path/to/your/audio/file.wav"
    ```

3. Run the script:

    ```bash
    python transcribe_and_generate_minutes.py
    ```

4. Follow the prompts to generate meeting minutes based on the transcribed audio.

## Example

Here is an example of how to use the script:

```bash
$ python transcribe_and_generate_minutes.py
Loaded API Key: your_api_key_here
{
    'abstract_summary': 'The meeting discussed...',
    'key_points': '1. Key point one\n2. Key point two...',
    'action_items': '1. Action item one\n2. Action item two...',
    'sentiment': 'The overall sentiment of the meeting was positive...'
}
