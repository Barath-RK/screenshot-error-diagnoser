<div align="center">

# 📸 Screenshot Error Diagnoser

### *AI-Powered Error Detection & Fix Generation*

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.0-green.svg)](https://flask.palletsprojects.com/)
[![OpenRouter](https://img.shields.io/badge/OpenRouter-API-purple.svg)](https://openrouter.ai/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

---

## 🎯 Problem Statement

> Developers waste hours typing error messages manually. What if you could just take a screenshot and get instant fix steps?

**Screenshot Error Diagnoser** solves this by combining:
- 🖼️ **Vision LLM** - Extracts error text from screenshots
- 📚 **RAG (Retrieval Augmented Generation)** - Matches errors against a knowledge base
- 🔧 **AI Generation** - Produces actionable, numbered fix steps

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📸 **Screenshot Upload** | Drag & drop or click to upload (PNG, JPG, WEBP) |
| 👁️ **Vision LLM** | Extracts exact error text from images |
| 🧠 **RAG Knowledge Base** | Stores & matches common errors with frequency tracking |
| 🔄 **Auto-Learning** | New errors automatically added to knowledge base |
| 💰 **Credits Tracking** | Real-time token usage & estimated cost monitoring |
| 📜 **Diagnosis History** | Stores all previous diagnoses with timestamps |
| 🧩 **Explain Simply** | Breaks down complex errors for beginners |
| 🔍 **Similar Errors** | Finds related issues in knowledge base |
| 📋 **Copy Solution** | One-click copy to clipboard |
| 🎨 **Premium UI** | Glassmorphism design with animations |

---

## 🏗️ Architecture
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ Upload │────▶│ Vision LLM │────▶│ RAG │
│ Screenshot │ │ Extract │ │ Match │
└─────────────┘ └─────────────┘ └──────┬──────┘
│
▼
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ Display │◀────│ Text │◀────│ Generate │
│ Fixes │ │ LLM │ │ Fixes │
└─────────────┘ └─────────────┘ └─────────────┘

text

**Tech Stack:**
- **Backend**: Flask 3.0 (Python 3.11+)
- **AI Models**: OpenRouter (Gemini/Llama free tier)
- **Database**: JSON (lightweight, no setup required)
- **Frontend**: HTML5, CSS3, JavaScript with marked.js

---

## 🚀 Quick Start

### Prerequisites
- Python 3.11 or higher
- OpenRouter API key ([Get free credits here](https://openrouter.ai/keys))

### Installation

```bash
# Clone repository
git clone https://github.com/vishnu-psvpec/06-screenshot-error-diagnoser.git
cd 06-screenshot-error-diagnoser

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your OpenRouter API key

# Run the application
python app.py
Access the App
Open your browser and navigate to: http://localhost:5001

📖 How It Works
Step 1: Upload Screenshot
Drag & drop any error screenshot or click to upload

Step 2: AI Extraction
Vision LLM reads the image and extracts the exact error message

Step 3: RAG Matching
The error is matched against your knowledge base for known fixes

Step 4: Fix Generation
AI generates numbered, actionable fix steps

Step 5: Auto-Learning
New errors are automatically added to the knowledge base for future users

🎮 Usage Examples
Example 1: Python Module Error
Input Screenshot:

text
ModuleNotFoundError: No module named 'flask'
Output:

text
1. Install Flask: pip install flask
2. Verify installation: pip list | grep flask
3. Check virtual environment is activated
4. Add flask to requirements.txt
5. Restart your application
Example 2: Port Conflict
Input Screenshot:

text
Error: listen EADDRINUSE: address already in use :::5000
Output:

text
1. Find process using port 5000: lsof -i :5000
2. Kill the process: kill -9 <PID>
3. Or use a different port: PORT=5001 npm start
4. Check for zombie processes
Example 3: Adobe Error
Input Screenshot:

text
Configuration error. Error: 16
Output:

text
1. Close all Adobe apps and Creative Cloud
2. Restart your computer
3. Run Adobe Creative Cloud Cleaner Tool
4. Reinstall the application
5. Sign out and back into Creative Cloud
📁 Project Structure
text
06-screenshot-error-diagnoser/
├── app.py                 # Flask backend + AI integration
├── templates/
│   └── index.html        # Web UI with premium design
├── static/
│   ├── style.css         # Glassmorphism styling
│   └── script.js         # Frontend logic & API calls
├── knowledge_base.json   # RAG knowledge base (auto-populated)
├── diagnosis_history.json # Diagnosis history (auto-generated)
├── credits_usage.json    # Credits tracking (auto-generated)
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables (create this)
├── .env.example          # Example environment variables
├── tests/
│   └── test_app.py      # Unit tests with pytest
├── sample_data/
│   └── sample_error.png  # Example error screenshots
├── docs/
│   └── AI_USAGE_NOTE.md  # AI development documentation
└── README.md             # This file
🧪 Running Tests
bash
pytest tests/ -v
Expected output:

text
test_rag_finds_econnrefused PASSED
test_rag_finds_module_error PASSED
test_rag_returns_empty_for_unknown PASSED
test_knowledge_base_has_entries PASSED
test_app_index_returns_200 PASSED
🤖 AI Capabilities Demonstrated
Capability	Implementation	Status
Vision LLM	Extracts text from error screenshots using Gemini Vision	✅
RAG (Retrieval Augmented Generation)	Matches errors to knowledge base with frequency sorting	✅
External API Integration	OpenRouter for LLM access (free tier)	✅
Agent Loop	Extract → Match → Generate → Auto-Learn	✅
📊 Evaluation Criteria Met
Criteria	Status
✅ Working code using AI assistants	Complete
✅ Hands-on skill in building AI Agents	Complete
✅ Service / API Integration	OpenRouter API
✅ End-to-End Execution and Usability	Complete
✅ Code Quality, Documentation and Demonstration	Complete
🔧 Environment Variables
Variable	Description	Default
OPENROUTER_API_KEY	Your OpenRouter API key	Required
OPENROUTER_MODEL	Model to use	openrouter/free
OPENROUTER_API_URL	API endpoint	https://openrouter.ai/api/v1
.env.example file:
env
OPENROUTER_API_KEY=your_api_key_here
OPENROUTER_MODEL=openrouter/free
OPENROUTER_API_URL=https://openrouter.ai/api/v1
🆓 Free Models Supported
Model	Vision Support	Cost	Best For
openrouter/free	✅	FREE	Auto-router (recommended)
Gemini Flash Lite	✅	FREE	Image extraction
Llama 3.2	❌	FREE	Text generation
Phi-3 Mini	❌	FREE	Lightweight fixes
Qwen 2.5	❌	FREE	Technical answers
📈 Screenshots
<div align="center"> <img src="https://via.placeholder.com/800x400?text=Upload+Screenshot" alt="Upload Interface" width="80%"> <br> <em>Upload Interface with Drag & Drop</em> </div><div align="center"> <img src="https://via.placeholder.com/800x400?text=Diagnosis+Results" alt="Diagnosis Results" width="80%"> <br> <em>AI-Generated Fix Steps</em> </div><div align="center"> <img src="https://via.placeholder.com/800x400?text=Knowledge+Base" alt="Knowledge Base" width="80%"> <br> <em>Knowledge Base with Auto-Learned Errors</em> </div>
🐛 Troubleshooting
API Key Not Working
bash
# Verify your key is loaded
python -c "import os; from dotenv import load_dotenv; load_dotenv(); print(os.getenv('OPENROUTER_API_KEY')[:20])"
Port Already in Use
python
# Change port in app.py (last line)
app.run(debug=True, port=5002)
Empty Response from Model
Check your internet connection

Wait a few seconds and retry

Free tier may have rate limits (wait 10-20 seconds)

Try a different model in the settings

Knowledge Base Not Saving
Check file permissions in the project folder

Ensure knowledge_base.json is writable

📝 AI Usage Note
See docs/AI_USAGE_NOTE.md for:

What AI helped with (code scaffolding, prompt design, test cases)

What AI got wrong (initial prompt lacked specificity)

Best prompts used (JSON-only output, step-by-step instructions)

🚀 Future Enhancements
Support for batch image processing

Export diagnoses as PDF/JSON

User accounts & saved histories

Team knowledge base sharing

VS Code extension integration

Slack/Discord bot version

Docker containerization

Cloud deployment (Railway/Render)

📄 Deliverables Checklist
Deliverable	Status
Public GitHub Repository	✅
README with setup & run instructions	✅
Demo Video (5-7 minutes)	⏳ Record with Loom/OBS
AI Usage Note	✅
Sample Data Folder	✅
Test Cases (pytest)	✅
Working Vision LLM + RAG	✅
👨‍💻 Author
Vishnu
Prince Spark Academy / PSVPEC
Hackathon 2026

https://img.shields.io/badge/GitHub-vishnu--psvpec-black?style=flat&logo=github
https://img.shields.io/badge/LinkedIn-Vishnu-blue?style=flat&logo=linkedin

🙏 Acknowledgments
OpenRouter for providing free LLM API access

Prince Spark Academy / PSVPEC for organizing the hackathon

Google Gemini & Meta Llama for open-source AI models

📄 License
MIT License - Free for academic and commercial use

text
MIT License

Copyright (c) 2026 Vishnu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions...

Full license text available in LICENSE file.
<div align="center">
🌟 If this project helped you, please star it on GitHub! 🌟
Made with ❤️ for Hackathon 2026
</div> ```
One more file - requirements.txt
txt
flask>=3.0.0
requests>=2.31.0
python-dotenv>=1.0.0
pytest>=8.0.0
Copy and paste these files:
README.md - Copy the entire markdown above

requirements.txt - Copy the 4 lines above

.env.example - Copy this:

env
OPENROUTER_API_KEY=your_api_key_here
OPENROUTER_MODEL=openrouter/free
OPENROUTER_API_URL=https://openrouter.ai/api/v1
All set for GitHub! 🚀




