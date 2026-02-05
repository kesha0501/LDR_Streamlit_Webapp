# 🛡️ Legal Document Redaction - Streamlit Web App

A powerful web application for redacting sensitive information from legal documents using BERT-NER (Named Entity Recognition) AI model. This tool automatically identifies and redacts Person Names (PER), Organizations (ORG), and Locations (LOC) from your documents.

[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-FFD21E?style=for-the-badge)](https://huggingface.co/)

## ✨ Features

- 📄 **Multiple File Format Support**: Upload PDF, Word (DOCX), or plain text files
- ✍️ **Text Paste Option**: Directly paste text for quick redaction
- 🎯 **Selective Entity Redaction**: Choose which entity types to redact (PER, ORG, LOC)
- 🤖 **AI-Powered**: Uses fine-tuned Legal BERT-NER model for accurate entity recognition
- 💾 **Download Results**: Export redacted text as a .txt file
- 🎨 **Beautiful UI**: Modern, user-friendly interface with custom styling
- ⚡ **Fast Processing**: Efficient token-based classification
- 🔒 **Privacy-Focused**: All processing happens locally, no data sent to external servers

## 🚀 Demo

The app provides a side-by-side view of your original and redacted documents:
- **Left Panel**: Original text
- **Right Panel**: Redacted text with sensitive information replaced by █ characters

## 📋 Prerequisites

- Python 3.8 or higher
- 4GB+ RAM recommended (for model loading)
- Internet connection (first run only, to download the model)

## 🔧 Installation

1. **Clone the repository**
```bash
git clone https://github.com/kesha0501/LDR_Streamlit_Webapp.git
cd LDR_Streamlit_Webapp
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the application**
```bash
streamlit run app.py
```

The app will automatically download the BERT-NER model (~400MB) on first run.

## 📦 Dependencies

- `streamlit` - Web application framework
- `pypdf` - PDF text extraction
- `python-docx` - Word document processing
- `transformers` - Hugging Face transformers for NER
- `torch` - PyTorch for model inference

## 🎮 Usage

1. **Launch the app** using `streamlit run app.py`
2. **Choose input method**:
   - Upload a file (PDF, DOCX, or TXT)
   - Or paste text directly
3. **Select entities to redact** from the sidebar:
   - PER (Person Names)
   - LOC (Locations)
   - ORG (Organizations)
4. **View results** side-by-side
5. **Download** the redacted text file

## 🧠 Model Information

**Model**: [sayeedlearnstech/LDR-NER_legal-BERT_fine_tuned](https://huggingface.co/sayeedlearnstech/LDR-NER_legal-BERT_fine_tuned)

This model is a fine-tuned BERT model specifically trained for legal document entity recognition. It identifies:
- **PER**: Person names (individuals, lawyers, judges, etc.)
- **LOC**: Geographic locations (cities, countries, addresses)
- **ORG**: Organizations (companies, law firms, government agencies)

## 📂 Project Structure

```
LDR_Streamlit_Webapp/
├── app.py                      # Main Streamlit application
├── inference_script.py         # BERT-NER model inference logic
├── requirements.txt            # Python dependencies
├── .streamlit/
│   └── config.toml            # Streamlit configuration
├── .gitignore                 # Git ignore rules
└── README.md                  # Project documentation
```

## ⚙️ Configuration

The app's appearance and behavior can be customized in `.streamlit/config.toml`:
- Theme colors
- Maximum upload size (default: 200MB)
- Error display settings
- Toolbar mode

## 🔐 Privacy & Security

- **Local Processing**: All redaction happens on your machine
- **No Data Storage**: Documents are processed in memory and not saved
- **No External Calls**: After model download, no internet connection needed

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the MIT License.

## 🐛 Known Issues

- First run requires internet connection to download the model
- Large PDF files may take longer to process
- Some PDF files with complex formatting may not extract text correctly

## 📧 Contact

For issues or questions, please open an issue on GitHub.

## 🙏 Acknowledgments

- Model by [sayeedlearnstech](https://huggingface.co/sayeedlearnstech)
- Built with [Streamlit](https://streamlit.io/)
- Powered by [Hugging Face Transformers](https://huggingface.co/transformers/)

---

⭐ If you find this project useful, please consider giving it a star!
