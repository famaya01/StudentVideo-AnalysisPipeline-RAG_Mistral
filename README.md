# AP4_ITIL_Video

## Description
This repository contains an end-to-end analysis pipeline designed to analyze student videos using a local German Language Model (LLM). The pipeline automates the process of extracting audio from video files, transcribing the audio to text, analyzing the text with predefined prompts, and querying a Retrieval-Augmented Generation (RAG) system. The final responses are saved in DOCX files.

## Workflow

1. **Video Input**:
    - Input student video files into the pipeline.

2. **Audio Extraction**:
    - Audio is extracted from the video files and saved using `ffmpeg`.

3. **Transcription**:
    - Extracted audio is transcribed into text using Whisper.

4. **Text Analysis**:
    - Transcribed text is analyzed using predefined prompts.
    - A RAG system with a local German LLM is used for querying and retrieving relevant information.

5. **Response Documentation**:
    - Analysis responses are saved in a structured DOCX file.

## Installation and Requirements

- Python 3.9 or higher
- Jupyter Notebook
- Download `em_german_leo_mistral` from [HuggingFace](https://huggingface.co/TheBloke/em_german_leo_mistral-GGUF/blob/main/em_german_leo_mistral.Q4_K_M.gguf) and place it in the `models` folder in the repository directory.

- `venv` module [installation guide](https://virtualenv.pypa.io/en/latest/installation.html)
- Set up a virtual environment and install dependencies:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```
- Ensure `ffmpeg` is installed and added to your system's PATH [installation link](https://ffmpeg.org/download.html). If your Python script cannot find `ffmpeg`, you can manually add `ffmpeg.exe` to the `venv\Scripts` directory.
- `llama-cpp-python` requires a C compiler:
  - Linux: gcc or clang
  - Windows: Visual Studio or MinGW
  - MacOS: Xcode

## Usage

1. **Launch Jupyter Notebook**:

    - Open `video_analysis_pipeline.ipynb`.

2. **Define the Path of the Video**:
    - In the notebook, locate the cell where the video path is defined.
    - Modify the `video_path` variable to point to the location of your video file. For example:
    ```python
    video_path = r"Path\To\Your\Video\File.mp4"
    ```

3. **Modify Prompts**:
    - The prompts used for text analysis are stored in `prompts.json`.
    - You can modify the prompts based on your needs by editing this file.

4. **Run the Pipeline**:
    - Execute the cells in the Jupyter notebook to start the analysis.
    - Follow the instructions in the notebook to run each step of the pipeline.

5. **Review Results**:
    - The DOCX files with the analysis results will be saved in the specified output directory.

## Roadmap

- Add visual analysis of the videos to enhance the overall analysis pipeline.

## Contact

Fatima Maya - [famaya@uni-bremen.de](mailto:famaya@uni-bremen.de)
