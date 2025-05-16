# QuickSee AI

**QuickSee AI** is a browser-based application that uses a webcam feed and a local vision-language model (VLM) to analyze real-time video frames and generate contextual responses to various prompts. It leverages Hugging Face's `transformers.js` library with WebGPU acceleration to run models entirely in-browser without sending data to external servers.

## 🚀 Features

- Real-time camera capture and processing
- Run vision-language models locally (no backend required)
- Choose from multiple natural language instructions like:
  - "What do you see?"
  - "Describe the environment"
  - "What's happening here?"
  - "Detect objects"
  - "Analyze the scene"
- Adjustable interval for frame analysis
- Fully client-side using WebGPU and WebAssembly

## 🧠 Model Used

- [SmolVLM-500M-Instruct](https://huggingface.co/HuggingFaceTB/SmolVLM-500M-Instruct) from Hugging Face Transformers.js

## 🛠️ Technologies

- HTML, CSS, and Vanilla JavaScript
- WebGPU for on-device AI inference
- Hugging Face Transformers.js
- MediaDevices API for camera access

## 📸 How It Works

1. The user loads the model in-browser.
2. The application requests camera access.
3. The user selects an instruction prompt.
4. On clicking "Start Processing", video frames are captured at a defined interval.
5. The vision-language model analyzes the frame and returns a response.
6. The user can stop processing at any time.

## 🔧 Requirements

- A modern browser with **WebGPU** support (e.g., latest Chrome/Edge on supported devices)
- HTTPS or `localhost` to access the webcam
- Camera permission must be granted

## 📂 File Structure
- project-folder/
- ├── index.html # Main HTML file with embedded CSS and JS
- └── README.md # Project documentation


## ⚠️ Known Issues

- Not all browsers support WebGPU. For best results, use a recent version of Chrome.
- Ensure you are running the app on `https://` or `localhost` to access the camera.

## 🧪 Local Testing

1. Clone the repository:
   ```bash
   git clone https://github.com/explore-with-yasir/QuickSeeAI.git
   cd quicksee-ai
1. Start a local server (e.g., using Python):
   ```bash
   python -m http.server 8000
1. Open the app in your browser:
   ```bash
   http://localhost:8000


