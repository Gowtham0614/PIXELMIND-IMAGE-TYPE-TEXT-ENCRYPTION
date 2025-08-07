# 🔐 PixelMind – Image-Based File Encryption System

**PixelMind** is a next-generation encryption tool that converts sensitive text files into seemingly harmless images and compiles them into secure PDFs.  
Leveraging advanced steganography-inspired logic, PixelMind ensures your data stays hidden in plain sight while remaining easily retrievable.

---

## 📌 Highlights

- 🔒 **Text-to-Image Encryption** – Hide your text securely within images  
- 📁 **Multi-File Support** – Encrypt multiple files in one go  
- 📄 **PDF Compilation** – Bundle encrypted images into secure PDFs  
- 🔓 **Secure Decryption** – Retrieve original content using authentication  
- 🌐 **User-Friendly Web Interface** – Clean and intuitive interface for ease of use  
- 🧾 **Format Flexibility** – Compatible with common text formats (.txt, .md, .log, etc.)

---

## 🧰 Tech Stack

- **Backend**: Flask (Python)  
- **Database**: MongoDB  
- **Encryption & Processing**: Pillow, PyMuPDF  
- **AI Integration**: Groq LLaMA 3.3-70B Versatile  
- **Deployment**: Localhost (Flask Dev Server)

---

## ⚙️ Setup & Installation

### ✅ Prerequisites

- Python 3.6 or above  
- MongoDB 4.4+  
- `pip` and `virtualenv` (recommended)

---

### 📥 Installation Steps
# 1. Clone the repository
git clone https://github.com/UnisysUIP/2025-File-encryption.git
cd 2025-File-encryption

# 2. Install dependencies
pip install -r requirements.txt
🔑 Generate & Configure Environment
python
Copy
Edit
# 3. Generate a secret key
import secrets
print(secrets.token_hex(32))  # Copy this value
Then, create a .env file in the root directory and add the following:

env
Copy
Edit
# Flask Secret Key
SECRET_KEY=your_generated_secret_key

# MongoDB Connection
MONGODB_URI=mongodb://localhost:27017/

# Groq API for LLaMA3-70B
CHATBOT_API_KEY=your_groq_api_key
API_URL=https://api.groq.com/openai/v1/chat/completions

# Default Admin Login (change in production)
DFAULT_USERNAME=guest
DFAULT_PASSWORD=guest
▶️ Run the Application
bash
python run.py
Access in browser:
📍 http://localhost:5000

📁 Project Structure
````bash
Copy
Edit
PixelMind/
├── app.py                  # Flask app entry point
├── database.py             # MongoDB interaction
├── image_operations.py     # Image encryption/decryption logic
├── pdf_operations.py       # PDF generation logic
├── chatbot_service.py      # AI assistant (Groq integration)
│
├── templates/              # HTML templates
│   ├── login.html
│   ├── register.html
│   └── dashboard.html
│
├── static/                 # CSS/JS assets
├── uploads/                # Temporary file storage
├── .env                    # Environment variables
└── requirements.txt        # Python dependencies
````
🔐 Default Login
Use these default credentials to log in for testing:

makefile
Copy
Edit
Username: guest
Password: guest
🛡 Security Notice
⚠️ This project is intended for educational/demo purposes only.

Do not use in production without proper security enhancements

Always use HTTPS for deployments

Use strong credentials and secure MongoDB with authentication

Rotate secrets and API keys regularly

Consider adding 2FA and access controls

🔄 Contribution Guide
Fork the repository

Create a feature branch (git checkout -b feature/your-feature)

Commit your changes

Push to your fork (git push origin feature/your-feature)

Submit a Pull Request

👨‍💻 Contributors
Mohammed Faisar A – MdFaisar

Ram Kumar R – rkcoder7

Gowtham K – Gowtham0614

Rakshita K – Rakshita-31

🙌 Acknowledgments
Flask

Pillow (PIL)

PyMuPDF

MongoDB

Groq Cloud – LLaMA 3.3-70B
