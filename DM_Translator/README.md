# DM Translator - English to Telugu Translation System 🌏

🚀 **Professional AI-powered translation system using IndicTrans2 for accurate English to Telugu translation with training data management capabilities**

## 📋 Overview

DM Translator is a comprehensive Django web application that provides powerful English to Telugu translation capabilities along with training data management features. Built with the state-of-the-art **IndicTrans2** model from AI4Bharat, it offers superior translation quality specifically designed for Indian languages.

### Core Capabilities
1. **🔄 Translation Services**: PDF upload and direct text translation
2. **📚 Training Data Management**: Create, edit, and manage translation datasets  
3. **👥 User Management**: Authentication and personalized dashboard
4. **📊 Data Processing**: Automated text extraction and alignment tools

## ✨ Features

### 🔄 Translation Services
- **PDF Translation**: Upload English PDF documents (up to 10MB) for complete Telugu translation
- **Text Translation**: Direct text input with support for up to 5000 characters
- **Real-time Progress**: Live progress tracking with completion percentages
- **Background Processing**: Non-blocking translation with AJAX-based updates
- **Download Results**: Save translations as text files

### 📚 Training Data Management
- **Dataset Creation**: Create new training datasets with custom names
- **Data Editor**: Interactive editor for English-Telugu translation pairs
- **CSV Upload**: Import existing training data from CSV files
- **Data Export**: Download training datasets for external use
- **Bulk Management**: Add, edit, and delete multiple translation pairs

### 🎯 User Experience
- **Modern UI**: Clean, responsive design with Bootstrap 5 and custom styling
- **Animated Dashboard**: Interactive cards with hover effects and icons
- **Progress Indicators**: Real-time feedback during translation processes
- **Copy & Share**: Easy copy-to-clipboard functionality
- **Mobile Responsive**: Optimized for all device sizes

### 🔧 Technical Features
- **IndicTrans2 Integration**: Primary model (ai4bharat/indictrans2-en-indic-dist-200M)
- **Smart Fallback**: Automatic fallback to alternative models if needed
- **GPU/CPU Support**: Automatic device detection for optimal performance
- **Chunked Processing**: Efficient handling of long texts with sentence-based splitting
- **Session Management**: Secure user sessions and data persistence
- **Error Handling**: Robust error management and user feedback

## 🏗️ Architecture

### Translation Engine
- **Primary Model**: `ai4bharat/indictrans2-en-indic-dist-200M` (optimized for quality and speed)
- **Script Conversion**: Advanced Devanagari to Telugu script conversion
- **Text Processing**: Intelligent sentence splitting and preprocessing
- **Performance Optimization**: Memory-efficient model loading and caching

### Data Processing Pipeline
- **PDF Extraction**: PyPDF2-based text extraction with error handling
- **Text Cleaning**: Automated text normalization and formatting
- **Sentence Alignment**: Intelligent English-Telugu sentence pairing
- **Quality Control**: Built-in validation and error detection

## 📁 Project Structure

```
DM_Translator/
├── dm_translator/                    # Django project root
│   ├── dm_translator/               # Main project configuration
│   │   ├── settings.py              # Django settings and app configuration
│   │   ├── urls.py                  # Main URL routing
│   │   ├── wsgi.py                  # WSGI application entry point
│   │   └── asgi.py                  # ASGI application entry point
│   │
│   ├── accounts/                    # User authentication & dashboard
│   │   ├── templates/accounts/      # Account-related templates
│   │   │   ├── home.html           # Main dashboard with feature cards
│   │   │   └── login.html          # User login interface
│   │   ├── views.py                # Authentication views and dashboard
│   │   ├── urls.py                 # Account URL patterns
│   │   └── models.py               # User-related models
│   │
│   ├── translator/                  # Core translation functionality
│   │   ├── templates/translator/    # Translation interface templates
│   │   │   ├── home.html           # Translation options selection
│   │   │   ├── upload_pdf.html     # PDF upload interface
│   │   │   ├── translate_text.html # Text input interface
│   │   │   ├── result.html         # Translation results display
│   │   │   ├── training_data_list.html        # Training data management
│   │   │   ├── training_data_editor.html      # Interactive data editor
│   │   │   ├── upload_training_data.html      # Dataset upload interface
│   │   │   └── create_empty_dataset.html      # New dataset creation
│   │   ├── views.py                # Translation logic and data management
│   │   ├── utils.py                # IndicTrans2 integration and utilities
│   │   ├── forms.py                # Django forms for all interfaces
│   │   ├── models.py               # Training data models
│   │   └── urls.py                 # Translator URL patterns
│   │
│   ├── training/                    # Training data management app
│   │   ├── templates/training/      # Training-specific templates
│   │   ├── views.py                # Training data processing views
│   │   ├── models.py               # Training data models
│   │   └── urls.py                 # Training URL patterns
│   │
│   ├── IndicTrans2/                # IndicTrans2 model repository
│   │   ├── huggingface_interface/  # HuggingFace integration scripts
│   │   ├── inference/              # Model inference utilities
│   │   ├── scripts/                # Training and evaluation scripts
│   │   ├── model_configs/          # Model configuration files
│   │   └── README.md               # IndicTrans2 documentation
│   │
│   ├── media/                      # User uploaded files
│   │   └── uploads/                # PDF and data file uploads
│   │
│   ├── db.sqlite3                  # SQLite database
│   ├── manage.py                   # Django management script
│   └── fix_bom.py                  # Utility script for text encoding
│
├── environ/                        # Python virtual environment
│   ├── Scripts/                    # Virtual environment executables
│   ├── Lib/site-packages/         # Installed Python packages
│   └── pyvenv.cfg                  # Virtual environment configuration
│
├── requirements.txt                # Python dependencies
└── README.md                       # This documentation file
```

## 🚀 Quick Setup

### Prerequisites
- **Python 3.8+** (Python 3.10+ recommended)
- **pip** (Python package manager)
- **At least 4GB RAM** (8GB recommended for optimal performance)
- **2GB free disk space** (for model downloads)
- **Stable internet connection** (for initial model download)

### Installation Methods

#### Option 1: Automated Setup (Recommended)

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd DM_Translator
   ```

2. **Create and activate virtual environment**
   ```powershell
   python -m venv environ
   environ\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Setup Django database**
   ```bash
   cd dm_translator
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create media directories**
   ```bash
   mkdir media
   mkdir media\uploads
   ```

6. **Start the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   ```
   Open browser: http://127.0.0.1:8000
   ```

### First Run Setup
- The IndicTrans2 model (~800MB) will download automatically on first translation
- Initial translation may take 2-3 minutes as the model loads
- Subsequent translations will be much faster

## 📦 Dependencies

### Core Framework
```
Django==5.2.4              # Web framework and backend
```

### AI & Machine Learning
```
torch==2.7.1               # PyTorch for deep learning models
transformers==4.53.1       # HuggingFace transformers library
tokenizers==0.21.2         # Fast tokenizers for text processing
huggingface-hub==0.33.2    # HuggingFace model hub integration
```

### Document Processing
```
PyPDF2==3.0.1             # PDF text extraction
python-docx==1.2.0        # Word document processing
pdf2image==1.17.0         # PDF to image conversion
pytesseract==0.3.13       # OCR for image-based PDFs
```

### Text Processing & NLP
```
indic-nlp-library==0.92        # Indic language processing
indic-transliteration==2.3.69  # Script transliteration
nltk==3.9.1                    # Natural language toolkit
```

### Data & Utilities
```
numpy==2.2.6               # Numerical computing
pandas==2.3.0              # Data manipulation
pillow==11.3.0             # Image processing
requests==2.32.4           # HTTP requests
```

### Installation
All dependencies are automatically installed via:
```bash
pip install -r requirements.txt
```

## 🖥️ Usage Guide

### 1. Access the Application
1. Start the Django server: `python manage.py runserver`
2. Open browser: `http://127.0.0.1:8000`
3. Log in or create an account for personalized experience

### 2. Dashboard Overview
The main dashboard provides access to all features:
- **🔄 Translation Services**: PDF and text translation options
- **📚 Training Data Management**: Create and manage datasets
- **📊 Quick Actions**: Direct access to common tasks
- **💡 Recent Activity**: View your translation history

### 3. Translation Services

#### PDF Translation
1. Click **"Upload PDF"** from the dashboard
2. Select an English PDF file (max 10MB)
3. Click **"Translate PDF"**
4. Monitor real-time progress with animated indicators
5. View, copy, or download the Telugu translation

#### Text Translation
1. Click **"Type Text"** from the dashboard
2. Enter or paste English text (max 5000 characters)
3. Click **"Translate Text"**
4. Get instant Telugu translation
5. Use copy/download options for results

### 4. Training Data Management

#### Create New Dataset
1. Navigate to **"Training Data"** from dashboard
2. Click **"Create New Dataset"**
3. Enter dataset name and description
4. Start adding English-Telugu translation pairs

#### Interactive Data Editor
1. Select existing dataset or create new one
2. Use the interactive editor to:
   - Add new translation pairs
   - Edit existing entries
   - Delete unwanted entries
   - Preview translations in real-time

#### Import/Export Data
1. **Import**: Upload CSV files with English-Telugu pairs
2. **Export**: Download datasets for external use
3. **Validation**: Automatic data validation and error detection

### 5. Working with Results
- **Copy Functionality**: One-click copy to clipboard
- **Download Options**: Save as TXT files
- **Progress Tracking**: Real-time updates during processing
- **Error Handling**: Clear error messages and recovery options

## 🔧 Configuration & Customization

### Model Configuration
The system uses `ai4bharat/indictrans2-en-indic-dist-200M` by default. Modify in `translator/utils.py`:

```python
class IndicTrans2Translator:
    def __init__(self):
        self.model_name = "ai4bharat/indictrans2-en-indic-dist-200M"
        # Optimized for quality and speed balance
        # Alternative: "ai4bharat/indictrans2-en-indic-1B" for higher quality
```

### Performance Optimization
- **GPU Support**: Automatic GPU detection and utilization
- **Memory Management**: Efficient model loading and caching
- **Batch Processing**: Intelligent text chunking for large documents
- **Script Conversion**: Advanced Devanagari to Telugu conversion

### File Upload Limits
Customize upload limits in `translator/forms.py`:
```python
def clean_pdf_file(self):
    pdf_file = self.cleaned_data['pdf_file']
    if pdf_file.size > 10 * 1024 * 1024:  # Modify 10MB limit
        raise forms.ValidationError('File size should not exceed 10MB.')
```

### Database Configuration
The project uses SQLite by default. For production, consider PostgreSQL:
```python
# In settings.py
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'dm_translator',
        'USER': 'your_user',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

## 🧪 Testing & Development

### Available Test Tools
- **fix_bom.py**: Text encoding utility for UTF-8 BOM issues
- **test_indictrans_detailed.py**: Comprehensive model testing and diagnostics

### Manual Testing Checklist
1. **PDF Upload**: Test with various PDF formats and sizes
2. **Text Translation**: Verify different text lengths and complexities
3. **Training Data**: Test CRUD operations on datasets
4. **User Authentication**: Verify login/logout functionality
5. **UI Responsiveness**: Test on different screen sizes
6. **Error Handling**: Test with invalid inputs and edge cases

### Development Setup
```bash
# Enable DEBUG mode in settings.py
DEBUG = True

# Install development dependencies
pip install django-debug-toolbar

# Run with detailed logging
python manage.py runserver --verbosity=2
```

## 🛠️ Troubleshooting

### Common Issues & Solutions

#### 1. Model Loading Issues
**Problem**: IndicTrans2 model fails to load
**Solutions**:
- Ensure stable internet connection for first download
- Check available disk space (need ~2GB free)
- Verify PyTorch installation: `python -c "import torch; print(torch.__version__)"`
- Clear cache: Delete `~/.cache/huggingface/` folder

#### 2. Memory Issues
**Problem**: Out of memory during translation
**Solutions**:
- Reduce chunk size in `utils.py`: `max_chunk_size = 200`
- Close other applications to free RAM
- Use CPU instead of GPU for large texts
- Process shorter text segments

#### 3. PDF Processing Failures
**Problem**: PDF text extraction fails
**Solutions**:
- Ensure PDF contains selectable text (not scanned images)
- Check PDF file integrity and size
- Verify file is not password-protected
- Try converting to plain text first

#### 4. Telugu Text Display Issues
**Problem**: Telugu characters appear as boxes
**Solutions**:
- Install Telugu fonts: Noto Sans Telugu, Pothana2000
- Use modern browsers (Chrome 90+, Firefox 88+)
- Check system language support settings
- Verify UTF-8 encoding in browser

#### 5. Training Data Import Issues
**Problem**: CSV upload fails or data appears corrupted
**Solutions**:
- Ensure CSV has proper English,Telugu column headers
- Check for UTF-8 encoding in CSV file
- Verify no special characters in dataset names
- Remove empty rows from CSV files

### Performance Optimization Tips

#### For Large Datasets
```python
# In utils.py, adjust parameters for better performance
max_chunk_size = 300        # Increase for faster processing
beam_size = 2              # Reduce for speed, increase for quality
max_length = 400           # Adjust based on average sentence length
```

#### Memory Management
```python
# Clear model cache periodically
import gc
import torch
torch.cuda.empty_cache()
gc.collect()
```

### Debug Mode Commands
```bash
# Check Django configuration
python manage.py check

# Validate models
python manage.py validate

# View SQL queries
python manage.py sqlflush

# Test database connection
python manage.py dbshell
```

## 🤝 Contributing

We welcome contributions to improve DM Translator! Here's how you can help:

### Development Setup
1. Fork the repository
2. Clone your fork: `git clone <your-fork-url>`
3. Create development branch: `git checkout -b feature-name`
4. Set up development environment: `pip install -r requirements.txt`
5. Make your changes and test thoroughly
6. Submit a pull request with detailed description

### Contribution Areas
- **🔧 Translation Engine**: Improve model integration and performance
- **🎨 UI/UX**: Enhance user interface and experience
- **📚 Documentation**: Improve documentation and tutorials
- **� Bug Fixes**: Fix issues and improve stability
- **🌐 Localization**: Add support for more languages
- **📊 Analytics**: Add usage statistics and performance metrics

### Code Standards
- Follow PEP 8 for Python code
- Use meaningful variable and function names
- Add docstrings for complex functions
- Test your changes before submitting
- Update documentation as needed

## � License

This project is licensed under the **MIT License** - see the LICENSE file for details.

### Third-Party Licenses
- **IndicTrans2**: AI4Bharat License
- **Django**: BSD License
- **PyTorch**: BSD License
- **HuggingFace Transformers**: Apache 2.0 License

## 🙏 Acknowledgments

### Research & Models
- **[AI4Bharat](https://ai4bharat.iitm.ac.in/)** - IndicTrans2 model development
- **[HuggingFace](https://huggingface.co/)** - Transformers library and model hosting
- **[PyTorch](https://pytorch.org/)** - Deep learning framework

### Open Source Community
- **[Django](https://www.djangoproject.com/)** - Web framework
- **[Bootstrap](https://getbootstrap.com/)** - UI components
- **[Font Awesome](https://fontawesome.com/)** - Icons and graphics

### Language Resources
- **Telugu Language Community** - Feedback and validation
- **Indic NLP Library** - Text processing utilities
- **NLTK** - Natural language processing tools

## 📞 Support & Contact

### Getting Help
1. **Documentation**: Check this README and inline documentation
2. **Issues**: Create an issue in the repository for bugs/features
3. **Troubleshooting**: Follow the troubleshooting section above
4. **Testing**: Run diagnostic tools (`test_indictrans_detailed.py`)

### Community
- **Discussions**: Use GitHub Discussions for questions
- **Feature Requests**: Submit detailed feature requests via Issues
- **Bug Reports**: Include system info and reproduction steps

### Professional Support
For enterprise use or custom development, contact the development team.

## � Version History & Roadmap

### Current Version: 2.0.0
- ✅ Complete Django web application
- ✅ IndicTrans2 integration with optimized performance
- ✅ Modern responsive UI with Bootstrap 5
- ✅ Training data management system
- ✅ User authentication and session management
- ✅ PDF and text translation capabilities
- ✅ Real-time progress tracking
- ✅ Interactive training data editor

### Version 1.0.0 (Previous)
- ✅ Basic translation functionality
- ✅ Simple web interface
- ✅ PDF processing capabilities

### Roadmap (Future Versions)

#### Version 2.1.0 (Next Release)
- 🔄 API endpoints for external integration
- 🔄 Translation history and analytics
- 🔄 Batch file processing
- 🔄 Enhanced error reporting
- � Performance monitoring dashboard

#### Version 2.5.0 (Medium Term)
- 🔄 Multiple Indian language support
- � Advanced translation quality metrics
- 🔄 Custom model fine-tuning interface
- 🔄 Collaborative translation features
- 🔄 Cloud deployment guides

#### Version 3.0.0 (Long Term)
- 🔄 Real-time collaborative translation
- 🔄 Advanced analytics and reporting
- 🔄 Mobile application
- 🔄 Integration with popular document platforms
- 🔄 Enterprise-grade security features

### Feature Requests
Vote for features or suggest new ones via GitHub Issues with the "enhancement" label.

---

## � Quick Start Summary

1. **Install**: `pip install -r requirements.txt`
2. **Setup**: `python manage.py migrate`
3. **Run**: `python manage.py runserver`
4. **Access**: `http://127.0.0.1:8000`
5. **Translate**: Upload PDF or enter text

**Happy Translating! 🌟**

*Telugu: తెలుగు అనువాదం శుభాకాంక్షలు! 🎉*

---

**Made with ❤️ for the Telugu language community and AI research advancement**
