# 🚀 Gemini API Lab — First Gemini API Call

A beginner-friendly Python project that demonstrates how to connect a Python application with Google's Gemini API, securely store an API key, send a prompt, and display an AI-generated response.

## 📌 Objective

This project demonstrates how to:

* Set up a Python API project
* Create and use a virtual environment
* Install the Gemini Python SDK
* Securely store an API key using `.env`
* Send prompts to a Gemini AI model
* Receive and display AI-generated responses
* Experiment with different prompts

## 🛠️ Technologies Used

* **Python**
* **Google Gemini API**
* **Google GenAI Python SDK**
* **python-dotenv**
* **VS Code**
* **Git & GitHub**

## 📂 Project Structure

```text
gemini-api-lab/
│
├── app.py
├── .env
├── .gitignore
├── README.md
└── venv/
```

> ⚠️ `venv/` and `.env` should NOT be uploaded to GitHub.

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Go into the project folder:

```bash
cd gemini-api-lab
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

#### Windows PowerShell

```powershell
.\venv\Scripts\Activate.ps1
```

You should see:

```text
(venv) PS C:\...\gemini-api-lab>
```

### 4. Install dependencies

```bash
pip install google-genai python-dotenv
```

## 🔑 Gemini API Key Setup

Create a Gemini API key using:

**Google AI Studio:** https://aistudio.google.com/

Create a `.env` file in the project directory:

```env
GEMINI_API_KEY=your_api_key_here
```

Replace `your_api_key_here` with your actual API key.

### ⚠️ Security

**Never upload your API key to GitHub.**

Do not:

* Hard-code the API key in `app.py`
* Share the API key publicly
* Upload `.env`
* Put the API key in screenshots
* Commit API keys to GitHub

The `.gitignore` file protects the `.env` file from being committed.

## 💻 Application Code

The main program is contained in `app.py`:

```python
from google import genai
from dotenv import load_dotenv
import os

load_dotenv()

client = genai.Client(
    api_key=os.getenv("GEMINI_API_KEY")
)

response = client.models.generate_content(
    model="gemini-2.5-flash",
    contents="Explain artificial intelligence in one simple paragraph."
)

print(response.text)
```

## ▶️ Run the Project

After activating your virtual environment and configuring `.env`, run:

```bash
python app.py
```

The terminal will display the AI-generated response.

Example:

```text
Artificial intelligence is a field of computer science
that enables machines to perform tasks that normally
require human intelligence, such as learning, reasoning,
understanding language, and recognizing patterns.
```

## 🔄 How It Works

```text
Python Program
      ↓
Google GenAI Python SDK
      ↓
Gemini API
      ↓
Gemini AI Model
      ↓
Generated Response
      ↓
Python Program
      ↓
Terminal
```

## 🧪 Experiment With Prompts

You can change:

```python
contents="Explain artificial intelligence in one simple paragraph."
```

For example:

```python
contents="Explain cybersecurity to a beginner."
```

Or:

```python
contents="Write a Python program to check whether a number is prime."
```

Or:

```python
contents="Explain machine learning using a real-world example."
```

## 📦 Dependencies

The project uses:

```text
google-genai
python-dotenv
```

You can also create a `requirements.txt` file:

```text
google-genai
python-dotenv
```

Then install everything with:

```bash
pip install -r requirements.txt
```

## 🎯 Learning Outcomes

After completing this project, you will understand:

* How API-based AI applications work
* How to use the Gemini API with Python
* How to securely manage API credentials
* How to send prompts programmatically
* How to receive AI-generated responses
* How to use Git and GitHub for an API project

## 🔐 Important Note

This project is intended for educational purposes.

Keep your Gemini API key private and follow Google's current API usage, quota, and billing policies.

## 👨‍💻 Author

**Harshit Singh**

B.Tech CSE — Cybersecurity

## ⭐ Future Improvements

Possible improvements include:

* Add a command-line chatbot
* Build a web interface using Flask or FastAPI
* Add conversation history
* Add streaming responses
* Create a React frontend
* Connect the application to a database
* Deploy the application online

---

⭐ If you found this project useful, consider giving the repository a star!
