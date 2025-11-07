🧠 Text Summarizer & NLP Analyzer (Flask App)

This project is a Flask-based web application that performs text preprocessing, NLP analysis, and automatic summarization.
Users can input any paragraph, and the app will:

Clean and preprocess text

Perform stemming, lemmatization, POS tagging, and Named Entity Recognition (NER)

Generate a summary using a pre-trained model (pickle or Hugging Face pipeline)

🚀 Features

🧩 Text cleaning (removes URLs, special characters, extra spaces)

🔠 Tokenization, Stemming, and Lemmatization

🧾 Part-of-Speech tagging (POS)

🏷️ Named Entity Recognition (NER)

✨ Automatic text summarization

🖥️ Simple web interface with real-time results

🗂️ Project Structure
📦 text-summarizer-flask
│
├── app.py                 # Main Flask application
├── summarizer.pkl         # Pre-trained summarization model (pickle)
├── templates/
│   └── index.html         # Combined input + result HTML page
├── static/                # (optional) CSS, JS, or images
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies

⚙️ Installation & Setup
1. Clone the Repository
git clone https://github.com/yourusername/text-summarizer-flask.git
cd text-summarizer-flask

2. Create a Virtual Environment (recommended)
python -m venv venv
venv\Scripts\activate    # on Windows
# OR
source venv/bin/activate # on macOS/Linux

3. Install Dependencies
pip install -r requirements.txt


Example requirements.txt:

Flask
spacy
nltk
transformers
torch


Then install the SpaCy English model:

python -m spacy download en_core_web_sm

4. Add or Train Your Summarizer Model

Place your summarizer.pkl file in the project root.
(You can also modify the app to use a Hugging Face model instead of a pickle file.)

5. Run the App
python app.py


Then open your browser and visit:

http://127.0.0.1:5000/

🧩 Example Input

In recent years, the rise of artificial intelligence has transformed industries across the globe...

🧾 Example Output

Cleaned Text: AI-related cleaned version of the input

Stems & Lemmas: Root words extracted

POS Tags & Entities: Linguistic and named entity info

Summary: "Artificial intelligence is transforming industries by improving efficiency and accuracy across sectors."

🧰 Technologies Used

Python 3.8+

Flask – for the web framework

spaCy – for POS tagging and NER

NLTK – for tokenization and stemming

Transformers / Pickle model – for summarization

🧪 Testing

You can test the app using the following sample input:

Tesla reported record profits in the third quarter of 2024, driven by strong demand for its electric vehicles and increased production capacity in Berlin and Texas...

🛠️ Customization

To switch from a pickle model to a Hugging Face transformer, modify this part in app.py:

from transformers import pipeline
summarizer_model = pipeline("summarization")

summary = summarizer_model(cleaned_text, max_length=100, min_length=30, do_sample=False)[0]['summary_text']

🧩 Future Improvements

Support for multilingual text summarization

Integration with advanced transformer-based models (e.g., BART, T5, Pegasus)

Database for saving analysis history

REST API version for external use

👩‍💻 Author
HITHAISH K A

![Screenshot_7-11-2025_22617_127 0 0 1](https://github.com/user-attachments/assets/5709fe10-7e85-4095-afb1-295cb886b77c)


📧 your.email@example.com

🌐 GitHub Profile
