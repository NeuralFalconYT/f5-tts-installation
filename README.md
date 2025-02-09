# [F5-TTS](https://github.com/SWivid/F5-TTS) Installation Guide

## Prerequisites
Ensure you have Python installed (recommended version: 3.8 or higher).

## Step 1: Create a Folder and Set Up a Virtual Environment
Manually create a folder or use the command below (you can name it anything, e.g., `local`):
```sh
mkdir local
cd local
python -m venv myenv
```

Activate the virtual environment:
- **Windows:**
  ```sh
  myenv\Scripts\activate
  ```
- **Linux/macOS:**
  ```sh
  source myenv/bin/activate
  ```

## Step 2: Install PyTorch and TorchAudio
Check your CUDA version:
```sh
nvcc --version
```
Example output might indicate CUDA 11.8, 12.1, or 12.4.

### Install PyTorch and TorchAudio Based on CUDA Version
Visit the [PyTorch Get Started](https://pytorch.org/get-started/locally/) page for official guidance.

Example my cuda version is **CUDA 11.8**:
```sh
pip install torch==2.3.0+cu118 --extra-index-url https://download.pytorch.org/whl/cu118
pip install torchaudio==2.3.0+cu118 --extra-index-url https://download.pytorch.org/whl/cu118
```
or,
```
pip install torch torchaudio --index-url https://download.pytorch.org/whl/cu118
```

## Step 3: Install F5-TTS
```sh
git clone https://github.com/SWivid/F5-TTS.git
cd F5-TTS
pip install -e .
```

Ensure you are inside the virtual environment before proceeding.

## Step 4: Run F5-TTS Gradio Interface
### Basic Launch
```sh
f5-tts_infer-gradio
```

### Specify Port and Host
```sh
f5-tts_infer-gradio --port 7860 --host 0.0.0.0
```

### Share Link for Remote Access
```sh
f5-tts_infer-gradio --share
```

## Running F5-TTS Later
If you want to run F5-TTS later, follow these steps:
1. Navigate to the installation folder:
   ```sh
   cd path/to/your-folder
   ```
2. Activate the virtual environment:
   - **Windows:**
     ```sh
     myenv\Scripts\activate
     ```
   - **Linux/macOS:**
     ```sh
     source myenv/bin/activate
     ```
3. Run the F5-TTS interface:
   ```sh
   f5-tts_infer-gradio
   ```

## Notes
- Ensure your CUDA version is correctly installed and detected.
- Always activate the virtual environment before running the commands.
- If you encounter issues, check the official [F5-TTS GitHub repository](https://github.com/SWivid/F5-TTS) for troubleshooting.

---
Enjoy using F5-TTS for your text-to-speech projects!

