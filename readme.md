Text-to-Speech Generator
A simple Text-to-Speech (TTS) generator that allows users to upload a voice sample and generate speech using a deep learning model. This project runs on Flask (Backend) and HTML/CSS/JS (Frontend). The backend uses the XTTS v2 model for high-quality voice cloning and synthesis.

Features
✅ Upload a voice sample (up to 1 minute long)
✅ Enter text to synthesize speech
✅ Uses XTTS v2 for high-quality voice cloning
✅ Generates and plays the synthesized audio
✅ Download the generated speech file
✅ Uses Ngrok to expose the backend to the frontend
✅ Deployable on Google Colab

How to Run on Google Colab 🚀
1️⃣ Set Up the Environment
Run the following commands in a Google Colab notebook:

python
Copy
Edit
!pip install flask flask-cors torch torchaudio TTS pyngrok
2️⃣ Create Directories for Uploads & Outputs
python
Copy
Edit
import os
UPLOAD_FOLDER = "./uploads"
OUTPUT_FOLDER = "./outputs"
os.makedirs(UPLOAD_FOLDER, exist_ok=True)
os.makedirs(OUTPUT_FOLDER, exist_ok=True)
3️⃣ Run the Backend
Create a Python cell in Google Colab and paste the backend code.

✅ Set Your Ngrok Token First:
python
Copy
Edit
from pyngrok import ngrok
ngrok.set_auth_token("YOUR_NGROK_AUTH_TOKEN")
public_url = ngrok.connect(5000)
print(f"Ngrok Tunnel: {public_url}")
✅ Run the Flask App:
python
Copy
Edit
!python app.py
Once the backend is running, copy the Ngrok public URL from the output.

4️⃣ Update Frontend with the Ngrok URL
Edit the NGROK_URL in the frontend HTML file:

javascript
Copy
Edit
const NGROK_URL = "https://your-ngrok-url.ngrok-free.app";
5️⃣ Open index.html and Start Using the App 🎉
Project Structure 📂
php
Copy
Edit
📁 TTS-Generator
│── 📄 app.py          # Flask Backend
│── 📄 index.html      # Frontend UI
│── 📂 uploads        # Stores uploaded audio files
│── 📂 outputs        # Stores generated speech files
│── 📄 README.md       # Project Documentation
Example Usage 📌
Upload a voice sample (up to 1 min long).
Enter text to convert into speech.
Click Generate Speech.
Listen or download the synthesized audio.
Technologies Used 🛠️
Flask (Backend API)
TTS (XTTS v2) (Text-to-Speech Model)
Ngrok (Expose backend to the internet)
Torchaudio (Audio processing)
HTML, CSS, JavaScript (Frontend UI)
Issues & Improvements 🚀
Add support for multiple languages
Improve UI with modern frameworks like React
Implement a database for storing generated audio
Contributors 🤝
Feel free to contribute, suggest improvements, or report issues!

Enjoy Using This Text-to-Speech Generator! 🎙️🔥