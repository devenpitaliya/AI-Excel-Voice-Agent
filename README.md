# 🎤 AI Excel Voice Agent

A Streamlit-based AI-powered assistant that enables users to **interact with Excel files using voice commands**. Built with **LangChain**, **OpenAI GPT-4**, and **Speech Recognition**, this tool translates voice queries into intelligent data analysis and responds with spoken answers.

---
Please create your own ENV
## 📌 Features

- 🔊 **Voice Input:** Ask questions via your microphone in natural language.
- 🤖 **AI-Powered Understanding:** Uses OpenAI GPT-4 with LangChain's Pandas agent to interpret and respond to questions about Excel data.
- 📊 **DataFrame Exploration:** Automatically reads and interacts with the Excel sheet.
- 🔁 **Conversational Memory:** Maintains a session-based chat history.
- 🔈 **Audio Responses:** Converts answers into spoken responses using `gTTS`.
- 🧠 **Natural Language Querying:** No need to write SQL or formulas—just speak.
- ⚙️ **Customizable Excel File:** Easily swap out the data source with your own `.xlsx` file.

---

## 🖼️ Demo

> “How many invoices are marked as exceptions?”
>
> “List top 5 vendors with the most discrepancies.”
>
> “What is the total value of delayed invoices?”

---

## 🚀 How It Works

1. Load an Excel file using `pandas`.
2. Use `SpeechRecognition` to capture and convert voice input to text.
3. Use LangChain's `create_pandas_dataframe_agent` with OpenAI GPT-4 to interpret the question.
4. Output the response on screen **and** convert it to speech using `gTTS`.
5. Maintain chat history using Streamlit session state.

---

## 📂 File Structure

voice_data_agent.py
ExceptionInvoices.xlsx
requirements.txt
README.md

yaml
Copy
Edit

---

## 🛠️ Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/yourusername/ai-excel-voice-agent.git
   cd ai-excel-voice-agent
Set up a virtual environment

bash
Copy
Edit
python -m venv .venv
.venv\Scripts\activate  # Windows
Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
Add your OpenAI API key
Create a .streamlit/secrets.toml file:

toml
Copy
Edit
OPENAI_API_KEY = "your-openai-api-key-here"
Run the app

bash
Copy
Edit
streamlit run voice_data_agent.py
📦 Dependencies
streamlit

openpyxl

pandas

speechrecognition

gtts

langchain

langchain-openai

openai

🧪 Example Excel File
Place your Excel file at the specified path in the code or modify the path accordingly:

python
Copy
Edit
FILE_PATH = r"C:\path\to\ExceptionInvoices.xlsx"
💡 Use Cases
Business analysts analyzing invoice or finance reports

Accessibility tools for visually impaired users

Voice-controlled internal dashboards

Conversational UI for corporate data exploration

🧰 Tech Stack
Language: Python
UI: Streamlit
LLM: OpenAI GPT-4 via LangChain
Voice Recognition: SpeechRecognition (Google)
Text-to-Speech: gTTS
Data Handling: Pandas, Excel (openpyxl)

📌 To Do
 Add file upload via Streamlit UI

 Add support for multiple Excel sheets

 Improve multi-turn conversation memory

 Support CSV and Google Sheets

🙌 Credits
Built by Dev. Inspired by the intersection of voice technology and AI-powered data interfaces.

📃 License
License. Free to use, modify, and distribute.
