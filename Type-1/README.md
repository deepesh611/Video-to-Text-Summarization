# 🎥 Video Summarization (Type 1)

This project automatically generates a **text summary from a video** by analyzing its frames visually.  
It extracts key frames from the video, generates **captions** for each frame using a **BLIP (Bootstrapped Language Image Pretraining)** model, and then summarizes the combined text into a short paragraph.

---

## 🚀 Features
- 🎞️ **Frame Extraction:** Captures frames from the input video at regular intervals.  
- 🧠 **Vision-Language Model:** Uses the **BLIP model** from Hugging Face Transformers to describe each frame.  
- 📝 **Text Summarization:** Combines all frame captions and summarizes them into a short coherent text.  
- 💾 **Output:** Displays or saves both frame-level captions and the final video summary.

---

## 🧩 Tech Stack
- **Python 3.8+**
- **Libraries:**
  - `opencv-python` – for video frame extraction  
  - `torch`, `torchvision` – for deep learning  
  - `transformers` – for BLIP and summarization models  
  - `PIL` – for image handling  
  - `dotenv` – for environment configuration  
  - `numpy`, `json`, `os`, `requests`

---

## ⚙️ Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/video-summarization-type1.git
   cd video-summarization-type1
    ```

2. Run the Setup...

## 🧠 Usage

1. Place your video file (e.g. input.mp4) in the project folder.
2. Open and run the Jupyter Notebook:
3. The notebook will:
     - Extract frames from the video 
     - Generate captions using the BLIP model 
     - Combine captions and summarize them
4. The summary will be printed in the notebook output.

