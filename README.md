# PDF to Speech Converter

This Python script utilizes the Google Cloud Text-to-Speech API to convert text extracted from a PDF file into an MP3 audio file. The script reads a specified PDF file, extracts text from a selected page, and then synthesizes the text into speech.

## Prerequisites

- Python 3.x
- Install the required Python packages using:

    ```bash
    pip install google-cloud-texttospeech PyPDF2
    ```

- Create a Google Cloud project and enable the Text-to-Speech API. Obtain the API key and set up the necessary authentication for your environment.

## Usage

1. Clone the repository or download the script.
2. Replace `"put_your_file_name_here.pdf"` with the path to your PDF file.

    ```python
    PDF_TO_READ = "path/to/your/file.pdf"
    ```

3. Run the script:

    ```bash
    python pdf_to_speech.py
    ```

4. The script extracts text from the specified page, sends it to the Google Cloud Text-to-Speech API, and saves the resulting audio as an MP3 file ("output.mp3").

## Configuration

You can customize the PDF file to read by modifying the `PDF_TO_READ` variable. Additionally, adjust the voice parameters in the script (language, gender, audio encoding) according to your preferences.

```python
# Voice configuration
voice = texttospeech.VoiceSelectionParams(
    language_code="en-US", ssml_gender=texttospeech.SsmlVoiceGender.NEUTRAL
)

# Audio configuration
audio_config = texttospeech.AudioConfig(
    audio_encoding=texttospeech.AudioEncoding.MP3
)
```

## Important Note

Ensure that you have set up the necessary authentication for accessing the Google Cloud Text-to-Speech API. Refer to the [Google Cloud documentation](https://cloud.google.com/text-to-speech/docs/quickstart) for instructions on setting up authentication.
