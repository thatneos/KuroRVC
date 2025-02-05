# python rvc cli Documentation

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
   - [System Requirements](#system-requirements)
   - [Windows Installation](#windows-installation)
   - [Linux Installation](#linux-installation)
3. [Usage](#usage)
   - [Command-Line Options](#command-line-options)
   - [Usage Examples](#usage-examples)
4. [References](#references)
   - [Vocoders](#vocoders)
   - [VC Clients](#vc-clients)
   - [Pitch Extractors](#pitch-extractors)
   - [Other Tools and Libraries](#other-tools-and-libraries)
5. [Troubleshooting](#troubleshooting)
6. [Contributing](#contributing)
7. [Acknowledgments](#acknowledgments)

## Introduction

The `python-rvc-cli` is a command-line interface tool designed for voice conversion inference using RVC (Retrieval-based Voice Conversion). It is built to be simple and efficient, allowing users to easily convert voices using pre-trained models without delving into the complexities of model training. This tool is ideal for those who want to focus on inference tasks, leveraging existing models to achieve high-quality voice conversions.

## Installation

### System Requirements

- **Python 3.9** (Recommended)
- A compatible operating system (Windows or Linux)

### Windows Installation

1. **Download the Repository:**
   - Clone the repository using Git or download it as a ZIP file from GitHub.
   - Extract the contents to a directory on your system.

2. **Run the Installation Script:**
   - Navigate to the directory where you extracted the repository.
   - Locate the `install.bat` file.
   - Double-click the `install.bat` file to execute it. This script will set up a Conda environment with all necessary dependencies.

3. **Activate the Environment:**
   - After the script finishes, open a command prompt in the same directory.
   - To activate the Conda environment, run:
     ```bash
     conda activate
     ```
   - You should now be able to run the CLI tool using:
     ```bash
     env/python.exe rvc_cli.py
     ```

### Linux Installation

1. **Download the Repository:**
   - Clone the repository using Git or download it as a ZIP file from GitHub.
   - Extract the contents to a directory on your system.

2. **Run the Installation Script:**
   - Navigate to the directory where you extracted the repository.
   - Make the installation script executable by running:
     ```bash
     chmod +x install.sh
     ```
   - Execute the script:
     ```bash
     ./install.sh
     ```
   - This script will install all necessary dependencies and set up your environment.

3. **Run the CLI:**
   - After installation, you can run the tool using:
     ```bash
     python rvc_cli.py
     ```

## Usage

### Command-Line Options

The CLI provides several options to customize the voice conversion process. Use the `-h` flag to see a list of available options and their descriptions.

```bash
python rvc_cli.py -h
```

This will display the help message, detailing the various modes and parameters you can use.

### Usage Examples

1. **Basic Voice Conversion:**
   - Convert an audio file using a specific model.
   ```bash
   python rvc_cli.py --input input.wav --output output.wav --model hifi-gan
   ```

2. **Using Different Vocoders:**
   - Experiment with different vocoders to achieve varying voice qualities.
   ```bash
   python rvc_cli.py --input input.wav --output output.wav --vocoder vocos
   ```

3. **Extracting Pitch:**
   - Use a pitch extraction tool to analyze the input audio.
   ```bash
   python rvc_cli.py --input input.wav --extract-pitch --pitch-tool anyf0
   ```

4. **Downloading Audio:**
   - Download audio files from URLs for conversion.
   ```bash
   python download_audio.py --url https://example.com/audio.mp3 --output downloaded_audio.mp3
   ```

## References

The `python-rvc-cli` tool is built upon several open-source projects, each contributing to its functionality and efficiency.

### Vocoders

- **HiFi-GAN:** A powerful vocoder for high-fidelity voice synthesis.
  - Repository: [jik876/hifi-gan](https://github.com/jik876/hifi-gan)
- **Vocos:** Another high-quality vocoder for voice conversion.
  - Repository: [gemelo-ai/vocos](https://github.com/gemelo-ai/vocos)
- **BigVGAN & BigVSAN:** Advanced vocoders from NVIDIA and Sony.
  - Repositories: [NVIDIA/BigVGAN](https://github.com/NVIDIA/BigVGAN), [sony/bigvsan](https://github.com/sony/bigvsan)
- **vocoders by reppy4620:** A collection of various vocoding tools.
  - Repository: [reppy4620/vocoders](https://github.com/reppy4620/vocoders)
- **vocoder by fishaudio:** Additional vocoding tools for diverse applications.
  - Repository: [fishaudio/vocoder](https://github.com/fishaudio/vocoder)

### VC Clients

These projects provide the foundation and inspiration for the voice conversion techniques used in `python-rvc-cli`.

- **Retrieval-based-Voice-Conversion-WebUI:** The original project by RVC-Project.
  - Repository: [RVC-Project/Retrieval-based-Voice-Conversion-WebUI](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI)
- **So-Vits-SVC:** A robust voice conversion tool by svc-develop-team.
  - Repository: [svc-develop-team/so-vits-svc](https://github.com/svc-develop-team/so-vits-svc)
- **Mangio-RVC-Fork:** An enhanced fork of the original RVC project.
  - Repository: [Mangio621/Mangio-RVC-Fork](https://github.com/Mangio621/Mangio-RVC-Fork)
- **VITS by jaywalnut310:** A popular voice conversion model.
  - Repository: [jaywalnut310/vits](https://github.com/jaywalnut310/vits)
- **Harmonify by Eempostor:** A tool for harmonizing voices.
  - Hugging Face Model: [Eempostor/Harmonify](https://huggingface.co/Eempostor/Harmonify)

### Pitch Extractors

These tools are used for extracting pitch information from audio, crucial for accurate voice conversion.

- **RMVPE by Dream-High:** A real-time melody vocoder.
  - Repository: [Dream-High/RMVPE](https://github.com/Dream-High/RMVPE)
- **FCPE by CNChTu:** A fast and accurate pitch extractor.
  - Repository: [CNChTu/FCPE](https://github.com/CNChTu/FCPE)
- **CREPE by maxrmorrison:** A real-time pitch tracker.
  - Repository: [maxrmorrison/torchcrepe](https://github.com/maxrmorrison/torchcrepe)
- **AnyF0 by SoulMelody:** A versatile F0 extraction tool.
  - Repository: [SoulMelody/anyf0](https://github.com/SoulMelody/anyf0)

### Other Tools and Libraries

- **FAIRSEQ by facebookresearch:** A sequence modeling toolkit.
  - Repository: [facebookresearch/fairseq](https://github.com/facebookresearch/fairseq)
- **FAISS by facebookresearch:** A library for efficient similarity search.
  - Repository: [facebookresearch/faiss](https://github.com/facebookresearch/faiss)
- **ContentVec by auspicious3000:** For content-based voice conversion.
  - Repository: [auspicious3000/contentvec](https://github.com/auspicious3000/contentvec)
- **Audio Tools:**
  - **audio-slicer by openvpi:** For segmenting audio files.
    - Repository: [openvpi/audio-slicer](https://github.com/openvpi/audio-slicer)
  - **python-audio-separator by karaokenerds:** For separating vocals and instruments.
    - Repository: [karaokenerds/python-audio-separator](https://github.com/karaokenerds/python-audio-separator)
  - **ultimatevocalremovergui by Anjok07:** A GUI tool for vocal removal.
    - Repository: [Anjok07/ultimatevocalremovergui](https://github.com/Anjok07/ultimatevocalremovergui)
  - **yt-dlp by yt-dlp:** For downloading audio from YouTube.
    - Repository: [yt-dlp/yt-dlp](https://github.com/yt-dlp/yt-dlp)

## Troubleshooting

- **Dependency Issues:** Ensure all dependencies are correctly installed. If you encounter missing modules, reinstall the dependencies using the provided scripts.
- **Environment Activation:** Always activate the Conda environment before running the CLI in Windows. For Linux, ensure the installation script has correctly set up your environment.
- **Model Compatibility:** Some models might require specific versions of libraries. Check the model's documentation if you encounter compatibility issues.

## Contributing

Contributions are welcome! If you have improvements or fixes, feel free to fork the repository and submit a pull request. Ensure your changes are well-documented and tested.

## Acknowledgments

The `python-rvc-cli` tool stands on the shoulders of giants, leveraging the incredible work from the open-source community. Special thanks to all the developers and maintainers of the referenced projects for their contributions to voice conversion technology.
