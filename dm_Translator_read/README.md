# DM Translator - Professional AI Translation System 🌏

🚀 **Complete Django-based translation system using IndicTrans2 for accurate English to Telugu translation with comprehensive management features**

## 📋 Table of Contents

1. [Overview](#-overview)
2. [Features](#-features)
3. [System Requirements](#-system-requirements)
4. [Quick Start](#-quick-start)
5. [Admin Manual](#-admin-manual)
6. [User Manual](#-user-manual)  
7. [Deployment Manual](#-deployment-manual)
8. [Usage Manual](#-usage-manual)
9. [Troubleshooting](#-troubleshooting)
10. [Performance Optimization](#-performance-optimization)
11. [Support & Contributing](#-support--contributing)

## 🎯 Overview

DM Translator is a comprehensive Django web application that provides powerful English to Telugu translation capabilities along with training data management features. Built with the state-of-the-art **IndicTrans2** model from AI4Bharat, it offers superior translation quality specifically designed for Indian languages.

### Core Capabilities
1. **🔄 Translation Services**: PDF upload and direct text translation
2. **📚 Training Data Management**: Create, edit, and manage translation datasets  
3. **👥 User Management**: Authentication and personalized dashboard
4. **📊 Data Processing**: Automated text extraction and alignment tools
5. **🔧 Admin Interface**: Comprehensive backend management
6. **🚀 Production Ready**: Full deployment and monitoring capabilities

## ✨ Features

### 🔄 Translation Services
- **PDF Translation**: Upload English PDF documents (up to 100MB) for complete Telugu translation
- **Document Translation**: Support for PDF, DOCX, and TXT files with structure preservation
- **Text Translation**: Direct text input with support for up to 5000 characters
- **OCR Integration**: Automatic text extraction from image-based PDFs using Tesseract
- **Real-time Progress**: Live progress tracking with completion percentages
- **Background Processing**: Non-blocking translation with AJAX-based updates
- **Smart Document Processing**: Maintains original formatting and structure
- **Multiple Download Formats**: Save as TXT, DOCX, or Anu Script format
- **Ramabhadra Font**: Authentic Telugu typography for better readability

### 📚 Training Data Management
- **Dataset Creation**: Create new training datasets with custom names and descriptions
- **Multiple Import Methods**: Upload CSV files, create from translations, or start empty
- **Advanced Data Editor**: Interactive editor for English-Telugu translation pairs
- **Smart File Parsing**: Automatic detection of DM Translator, CSV, and simple text formats
- **Column Management**: Shift Telugu columns and reorganize data structure
- **Data Export**: Download training datasets as CSV for external use
- **Bulk Management**: Add, edit, and delete multiple translation pairs
- **Pagination & Search**: Browse datasets efficiently with search functionality
- **Document Type Detection**: Automatic file type recognition and badges
- **Status Management**: Draft → Verified → Exported workflow
- **Dataset Renaming**: Rename datasets with validation
- **Training Entry Management**: Individual entry creation, editing, and deletion
- **Devanagari Conversion**: Live preview of Telugu text in Devanagari script
- **Segment Processing**: Intelligent text segmentation for training data alignment

### 🎯 User Experience
- **Modern UI**: Clean, responsive design with Bootstrap 5 and custom styling
- **Animated Dashboard**: Interactive cards with hover effects and icons
- **Progress Indicators**: Real-time feedback during translation processes
- **Copy & Share**: Easy copy-to-clipboard functionality
- **Mobile Responsive**: Optimized for all device sizes
- **Health Monitoring**: Built-in health check endpoints
- **Document Structure Debugging**: Advanced debugging tools for document processing
- **Multi-format Downloads**: TXT, DOCX, and Anu Script format support
- **Unicode Conversion**: Telugu to Devanagari and Anu Script conversion tools
- **File Type Badges**: Visual indicators for different document types
- **Advanced Navigation**: Beautiful gradient navbar with animated hover effects
- **User Profile Dropdown**: Complete user management with profile and settings access
- **Toast Notifications**: Success/error messages with auto-dismiss functionality
- **Loading Animations**: Sophisticated processing indicators with step-by-step progress
- **Resizable Columns**: Interactive table columns with drag-and-resize functionality
- **Character Counter**: Real-time character counting with color-coded warnings
- **Quick Actions**: Paste, clear, and sample text loading for faster workflow
- **Method Selection Cards**: Visual selection interface for translation and dataset creation methods

### 🔧 Technical Features
- **IndicTrans2 Integration**: Primary model (ai4bharat/indictrans2-en-indic-1B)
- **Smart Fallback**: Automatic fallback to alternative models if needed
- **GPU/CPU Support**: Automatic device detection for optimal performance
- **Chunked Processing**: Efficient handling of long texts with sentence-based splitting
- **Session Management**: Secure user sessions and data persistence
- **Error Handling**: Robust error management and user feedback
- **Translation Corrections**: Database-backed correction system
- **Feedback Collection**: User feedback and rating system
- **Document Structure Preservation**: Maintains formatting across PDF, DOCX, and TXT files
- **Advanced OCR**: Tesseract integration for image-based PDF processing
- **Multiple File Format Support**: PDF, DOCX, TXT input with intelligent processing
- **Progress Tracking**: Real-time translation progress with session-based tracking
- **Unicode Processing**: Complete Telugu Unicode and legacy script support
- **Text Segmentation**: Intelligent sentence and paragraph boundary detection
- **Probability Matching**: Advanced text matching algorithms for translation alignment

### 📄 Advanced Document Processing
- **Structure Preservation**: Maintains original document layout and formatting
- **Multi-format Input**: PDF, DOCX, TXT files with intelligent content extraction
- **OCR Capabilities**: Extract text from image-based PDFs using Tesseract
- **HTML Conversion**: Convert documents to HTML for processing and back to native formats
- **Smart Text Matching**: Probability-based text segment matching for accurate translations
- **Document Debugging**: Advanced debugging tools to analyze document structure
- **Format-specific Processing**: Specialized handlers for PDF (PyPDF2), DOCX (python-docx), and TXT
- **Fallback Processing**: Multiple extraction methods with intelligent fallbacks
- **Translation Mapping**: Create precise translation maps for document reconstruction
- **Quality Preservation**: Maintain document quality through processing pipeline

## 📋 System Requirements

### Development Environment
- **OS**: Windows 10+, macOS 10.14+, Ubuntu 18.04+
- **Python**: 3.8 or higher
- **RAM**: Minimum 8GB (16GB+ recommended for ML models)
- **Storage**: 10GB+ free space
- **Network**: Stable internet connection

### Production Environment
- **OS**: Ubuntu 20.04+ LTS (recommended)
- **RAM**: Minimum 8GB (16GB+ recommended for ML models)
- **CPU**: 4+ cores
- **Storage**: 50GB+ SSD
- **Database**: PostgreSQL 12+
- **Web Server**: Nginx + Gunicorn
- **Network**: Stable internet connection, domain name

### Software Dependencies
**Core Framework:**
- Python 3.8+
- Django 5.2.4
- PostgreSQL 12+ (production)
- Git
- Virtual environment support

**Machine Learning & NLP:**
- PyTorch 2.7.1
- Transformers 4.53.1
- Tokenizers 0.21.2
- HuggingFace Hub 0.33.2
- NumPy 2.2.6
- Pandas 2.3.0
- NLTK 3.9.1

**Indic Language Support:**
- indic-nlp-library 0.92
- indic-transliteration 2.3.69

**Document Processing:**
- PyPDF2 3.0.1
- python-docx 1.2.0
- pdf2image 1.17.0
- pytesseract 0.3.13
- Pillow 11.3.0
- PyMuPDF 1.24.7
- BeautifulSoup4 4.12.3

**Production Stack:**
- Gunicorn 21.2.0
- WhiteNoise 6.6.0
- psycopg2-binary 2.9.9

**System Dependencies:**
- Tesseract OCR
- Poppler utilities

## 🚀 Quick Start

### Local Development Setup

1. **Clone the Repository**
```bash
git clone https://github.com/dmouli408/DM_Translator.git
cd DM_Translator/dm_translator
```

2. **Create Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Database Setup**
```bash
python manage.py migrate
python manage.py createsuperuser
```

5. **Run Development Server**
```bash
python manage.py runserver
```

6. **Access Application**
- Main App: http://127.0.0.1:8000/
- Admin Panel: http://127.0.0.1:8000/admin/

## 👨‍💼 Admin Manual

### Admin Interface Overview
The Django admin interface provides comprehensive management for the translation system.

### Models Registered

#### 1. TranslationCorrection
**Purpose**: Manage database-backed corrections for translation output

**Admin Features**:
- **List View**: Shows input text, correct output, type, priority, status, and usage count
- **Filtering**: Filter by input type, correction type, active status, priority, and creation date
- **Search**: Search within input text, correct output, and context tags
- **Inline Editing**: Modify priority and active status directly from the list view
- **Custom Actions**: Easy management of correction entries

**Fields**:
- `input_text`: Original text pattern (English or incorrect Telugu)
- `input_type`: ENGLISH | INCORRECT_TELUGU | DEVANAGARI | PATTERN
- `correct_output`: Correct Telugu translation
- `correction_type`: WORD | PHRASE | CHARACTER | PATTERN
- `priority`: Higher number = higher priority (affects application order)
- `is_active`: Enable/disable the correction
- `context_tags`: Comma-separated tags for categorization
- `usage_count`: Automatically tracked usage statistics

#### 2. TranslationFeedback
**Purpose**: Collect and manage user feedback on translations

**Admin Features**:
- **List View**: Shows original text, feedback type, rating, user, and processing status
- **Filtering**: Filter by feedback type, rating, processing status, and date
- **Search**: Search within all text fields and comments
- **Bulk Actions**: Mark multiple feedback items as processed/unprocessed
- **Custom Display**: Shortened text for better readability

**Fields**:
- `original_text`: Original English text
- `generated_translation`: System-generated Telugu translation
- `corrected_translation`: User-provided correction (if any)
- `feedback_type`: INCORRECT | PARTIAL | FORMATTING | SUGGESTION
- `rating`: 1-5 star rating
- `comments`: Additional user comments
- `is_processed`: Track if feedback has been reviewed

#### 3. Training Data Management
**Purpose**: Manage training datasets and entries

**Features**:
- View all training datasets
- Monitor dataset statistics
- Bulk operations on training entries
- Export capabilities
- User assignment tracking

### Admin Access Instructions

1. **Login**: Navigate to `http://127.0.0.1:8000/admin/` (development) or `https://your-domain.com/admin/` (production)
2. **Credentials**: Use superuser credentials created during setup
3. **Navigation**: Use the admin sidebar to access different models

### Admin URLs
- Main Admin: `/admin/`
- Translation Corrections: `/admin/translator/translationcorrection/`
- Translation Feedback: `/admin/translator/translationfeedback/`
- Training Datasets: `/admin/translator/trainingdataset/`
- Users: `/admin/auth/user/`

### Common Admin Tasks

#### Adding New Corrections
1. Go to Translation Corrections
2. Click "Add Translation Correction"
3. Fill in the input pattern and correct output
4. Set appropriate priority and type
5. Save

#### Managing User Feedback
1. Go to Translation Feedback
2. Review user submissions
3. Use bulk actions to mark as processed
4. Use feedback to create new corrections

#### Managing Training Data
1. Go to Training Datasets
2. View dataset statistics
3. Export data as needed
4. Monitor user activity

### Security Best Practices
- Change admin URL in production (optional)
- Use strong admin passwords
- Limit admin access to authorized personnel
- Regular admin activity monitoring
- Enable admin logging

## 👤 User Manual

### Getting Started

#### Account Creation
1. Visit the application homepage
2. Click "Register" to create an account
3. Fill in required information
4. Verify email (if email verification is enabled)
5. Login with your credentials

#### Dashboard Overview
After logging in, you'll see the main dashboard with:
- **Translation Options**: Text and PDF translation
- **Training Data**: Access to your datasets
- **Recent Activity**: Your translation history
- **Quick Actions**: Common tasks

### Translation Services

#### Text Translation
1. **Access**: Click "Translate Text" from dashboard
2. **Input**: Enter or paste English text (up to 5000 characters)
3. **Options**: Select translation settings if available
4. **Translate**: Click "Translate" button
5. **Results**: View side-by-side English and Telugu text
6. **Actions**: Copy, download, or share results

#### PDF Translation
1. **Access**: Click "Upload PDF" from dashboard
2. **Upload**: Select PDF file (up to 100MB)
3. **Processing**: Wait for text extraction and translation
4. **Progress**: Monitor real-time translation progress
5. **Results**: View translated content with original formatting
6. **Download**: Save translated document

#### Translation Features
- **Real-time Progress**: See translation progress as it happens
- **Copy to Clipboard**: Easy copying of translated text
- **Multiple Download Options**: Save as TXT, DOCX, or Anu Script format
- **Share Results**: Share translations via URL or social media
- **Quality Rating**: Rate translation quality to help improve the system
- **Document Structure Preservation**: Original formatting maintained in translations
- **OCR Support**: Automatic text extraction from image-based PDFs
- **Unicode Conversion**: Convert Telugu text to Devanagari or legacy Anu Script
- **Progress Session Management**: Resume translation progress across browser sessions

### Training Data Management

#### Creating Training Datasets
1. **Access**: Go to "Training Data" section
2. **New Dataset**: Click "Create New Dataset"
3. **Details**: Enter dataset name and description
4. **Source**: Choose creation method:
   - Upload CSV file
   - Create from translation result
   - Start with empty dataset
5. **Save**: Create the dataset

#### Managing Training Data
1. **View Datasets**: See all your training datasets
2. **Search**: Find specific datasets using search
3. **Filter**: Use filters for dataset type, status, etc.
4. **Edit**: Click on dataset to edit entries
5. **Export**: Download datasets as CSV

#### Training Data Editor
1. **Access**: Click "Edit" on any dataset
2. **Add Entries**: Manually add English-Telugu pairs
3. **Edit Entries**: Modify existing translations
4. **Delete Entries**: Remove incorrect entries
5. **Bulk Actions**: Import/export multiple entries
6. **Validation**: System checks for data quality
7. **Column Management**: Shift and reorganize Telugu columns
8. **Live Preview**: Real-time Devanagari conversion preview
9. **Smart Parsing**: Automatic format detection for uploaded files
10. **Segment Processing**: Advanced text segmentation and alignment

#### Dataset Workflow
1. **Draft**: Initial creation and data entry
2. **Verified**: Quality checked and approved
3. **Exported**: Ready for use in training

### Best Practices

#### For Translation
- **File Formats**: Supports PDF, DOCX, TXT files up to 100MB
- **Text Length**: Keep individual translations under 5000 characters for direct text input
- **Document Quality**: Use high-quality PDFs for best OCR results
- **Language**: Ensure source text is in clear English
- **Format**: Use proper punctuation and grammar
- **Structure**: Complex documents with tables and formatting are supported

#### For Training Data
- **Quality**: Ensure accurate English-Telugu pairs
- **Consistency**: Maintain consistent terminology
- **Context**: Add relevant context tags
- **Review**: Always review before marking as verified

### Troubleshooting Common Issues

#### Translation Problems
- **Slow Translation**: Check internet connection and file size
- **Poor Quality**: Use feedback system to report issues
- **Failed Upload**: Ensure file is supported format (PDF, DOCX, TXT) and under 100MB
- **Missing Text**: Check PDF quality and OCR requirements
- **Document Structure Issues**: Use debug endpoint to analyze document processing
- **Format Conversion Errors**: Verify document is not corrupted or password-protected
- **OCR Failures**: Ensure Tesseract is properly installed for image-based PDFs

#### Account Issues
- **Login Problems**: Reset password or contact admin
- **Access Denied**: Ensure proper permissions
- **Data Loss**: Check recent activity or contact support

## 🏗️ Deployment Manual

### Production Deployment Guide

This section covers complete production deployment on Ubuntu servers with PostgreSQL.

#### Pre-Deployment Checklist
- [ ] Ubuntu 20.04+ LTS server ready
- [ ] Domain name configured
- [ ] SSL certificate plan (Let's Encrypt recommended)
- [ ] Database credentials prepared
- [ ] Email settings configured (optional)

### Step 1: Server Setup

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install required packages
sudo apt install -y python3 python3-pip python3-venv postgresql postgresql-contrib nginx git

# Install additional dependencies for document processing
sudo apt install -y tesseract-ocr poppler-utils
```

### Step 2: PostgreSQL Database Setup

```bash
# Switch to postgres user
sudo -u postgres psql

# Create database and user
CREATE DATABASE dm_translator_db;
CREATE USER dm_translator_user WITH PASSWORD 'your_secure_password_here';
ALTER ROLE dm_translator_user SET client_encoding TO 'utf8';
ALTER ROLE dm_translator_user SET default_transaction_isolation TO 'read committed';
ALTER ROLE dm_translator_user SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE dm_translator_db TO dm_translator_user;

# Exit PostgreSQL
\q
```

### Step 3: Application Deployment

```bash
# Create application directory
sudo mkdir -p /var/www/dm_translator
cd /var/www/dm_translator

# Clone the repository
sudo git clone https://github.com/dmouli408/DM_Translator.git .

# Set ownership
sudo chown -R $USER:$USER /var/www/dm_translator

# Navigate to Django project
cd dm_translator

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Step 4: Environment Configuration

```bash
# Copy environment template
cp .env.production .env

# Edit environment file with your production settings
nano .env
```

**Update the following variables in `.env`:**

```bash
# Django Settings
SECRET_KEY=your-very-secure-secret-key-here-minimum-50-characters
DEBUG=False
ALLOWED_HOSTS=your-domain.com,www.your-domain.com

# Database Configuration
DB_ENGINE=django.db.backends.postgresql
DB_NAME=dm_translator_db
DB_USER=dm_translator_user
DB_PASSWORD=your_secure_password_here
DB_HOST=localhost
DB_PORT=5432

# File Paths
MEDIA_ROOT=/var/www/dm_translator/media
STATIC_ROOT=/var/www/dm_translator/static

# Email Configuration (Optional)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USE_TLS=True
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-app-password
ADMIN_EMAIL=admin@your-domain.com

# Security Settings (Enable after SSL setup)
SESSION_COOKIE_SECURE=True
CSRF_COOKIE_SECURE=True
SECURE_SSL_REDIRECT=True
```

### Step 5: Django Application Setup

```bash
# Load environment variables
export $(cat .env | xargs)

# Run migrations
python manage.py makemigrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Collect static files
python manage.py collectstatic --noinput

# Create required directories
mkdir -p media/uploads media/temp_uploads logs
sudo chown -R www-data:www-data media/
sudo chown -R www-data:www-data logs/
```

### Step 6: Gunicorn Configuration

Create Gunicorn service file:

```bash
sudo nano /etc/systemd/system/dm_translator.service
```

Add the following content:

```ini
[Unit]
Description=DM Translator Django Application
After=network.target

[Service]
User=www-data
Group=www-data
WorkingDirectory=/var/www/dm_translator/dm_translator
Environment="PATH=/var/www/dm_translator/dm_translator/venv/bin"
EnvironmentFile=/var/www/dm_translator/dm_translator/.env
ExecStart=/var/www/dm_translator/dm_translator/venv/bin/gunicorn \
          --workers 3 \
          --bind unix:/run/gunicorn/dm_translator.sock \
          dm_translator.wsgi:application

[Install]
WantedBy=multi-user.target
```

Create Gunicorn socket directory:

```bash
sudo mkdir -p /run/gunicorn
sudo chown www-data:www-data /run/gunicorn
```

### Step 7: Nginx Configuration

```bash
sudo nano /etc/nginx/sites-available/dm_translator
```

Add the following configuration:

```nginx
server {
    listen 80;
    server_name your-domain.com www.your-domain.com;

    # Security headers
    add_header X-Content-Type-Options nosniff;
    add_header X-Frame-Options DENY;
    add_header X-XSS-Protection "1; mode=block";

    # File upload limit
    client_max_body_size 100M;

    location = /favicon.ico { access_log off; log_not_found off; }
    
    location /static/ {
        root /var/www/dm_translator;
        expires 1y;
        add_header Cache-Control "public, immutable";
    }

    location /media/ {
        root /var/www/dm_translator;
        expires 1y;
        add_header Cache-Control "public";
    }

    location / {
        include proxy_params;
        proxy_pass http://unix:/run/gunicorn/dm_translator.sock;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

Enable the site:

```bash
sudo ln -s /etc/nginx/sites-available/dm_translator /etc/nginx/sites-enabled/
sudo nginx -t
```

### Step 8: Start Services

```bash
# Start and enable Gunicorn
sudo systemctl start dm_translator
sudo systemctl enable dm_translator

# Restart Nginx
sudo systemctl restart nginx
sudo systemctl enable nginx

# Check service status
sudo systemctl status dm_translator
sudo systemctl status nginx
```

### Step 9: SSL Configuration (Recommended)

```bash
# Install Certbot
sudo apt install certbot python3-certbot-nginx

# Get SSL certificate
sudo certbot --nginx -d your-domain.com -d www.your-domain.com

# Test renewal
sudo certbot renew --dry-run
```

After SSL setup, update `.env`:

```bash
SESSION_COOKIE_SECURE=True
CSRF_COOKIE_SECURE=True
SECURE_SSL_REDIRECT=True
```

Then restart the application:

```bash
sudo systemctl restart dm_translator
```

### Step 10: Firewall Configuration

```bash
# Configure UFW firewall
sudo ufw allow OpenSSH
sudo ufw allow 'Nginx Full'
sudo ufw --force enable
```

### Post-Deployment Configuration

#### IndicTrans2 Model Setup
The application uses IndicTrans2 for translation. Models are loaded automatically, but for better performance:
1. Ensure adequate RAM (16GB+ recommended)
2. Models will be downloaded on first use
3. Monitor initial startup time

#### Test Translation
1. Access the application: `https://your-domain.com/`
2. Upload a test document
3. Verify translation functionality
4. Check admin interface access

## 📖 Usage Manual

### API Endpoints

#### Health Check Endpoints
```bash
# Basic health check
GET /health/

# Detailed system status
GET /api/status/
```

#### Translation Endpoints
```bash
# Text translation
POST /translator/translate-text/

# Unified PDF/Document upload
POST /translator/upload-pdf/

# Get translation progress
GET /translator/progress/<session_id>/

# Get translation result
GET /translator/result/<session_id>/
```

#### Training Data Endpoints
```bash
# List datasets
GET /translator/training-datasets/

# Create dataset
POST /translator/create-training-dataset/

# Create empty dataset
POST /translator/create-empty-dataset/

# Edit dataset
GET /translator/edit-training-data/<uuid:dataset_id>/

# Add training entry
POST /translator/add-training-entry/<uuid:dataset_id>/

# Delete training dataset
POST /translator/delete-training-dataset/<uuid:dataset_id>/

# Delete training entry
POST /translator/delete-training-entry/<uuid:entry_id>/

# Upload training data
POST /translator/upload-training-data/

# Export dataset
GET /translator/export-training-data/<uuid:dataset_id>/csv/

# Shift Telugu column
POST /translator/shift-telugu-column/<uuid:dataset_id>/

# Rename dataset
POST /translator/rename-training-dataset/<uuid:dataset_id>/
```

#### Document Processing Endpoints
```bash
# Download translated document
GET /translator/download-translation/<uuid:dataset_id>/

# Download simple Telugu DOCX
GET /translator/download-simple-telugu-docx/<uuid:dataset_id>/

# Debug document structure
GET /translator/debug-document-structure/<uuid:dataset_id>/
```

#### Utility Endpoints
```bash
# Convert Telugu to Devanagari
POST /translator/convert-telugu-to-devanagari/

# Download Anu Script format
POST /translator/download-anu-script/

# Debug endpoint
GET /translator/debug/
```

### Command Line Usage

#### Management Commands
```bash
# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Collect static files
python manage.py collectstatic

# Check system
python manage.py check

# Run tests
python manage.py test
```

#### Database Operations
```bash
# Database backup
python manage.py dumpdata > backup.json

# Database restore
python manage.py loaddata backup.json

# Clear cache
python manage.py clear_cache
```

### Configuration Options

#### Translation Settings
- **Progress Tracking**: Enable/disable real-time progress
- **Maximum File Size**: Configure upload limits
- **Timeout Settings**: Adjust processing timeouts
- **Model Selection**: Choose translation models

#### Performance Settings
- **Workers**: Adjust Gunicorn worker count
- **Cache Settings**: Configure Redis/Memcached
- **Database Pool**: Set connection pooling
- **Static Files**: Configure CDN if needed

### Integration Options

#### Fine-tuning IndicTrans2
You can fine-tune the IndicTrans2 model with your verified training data:

1. **Export Training Data**: Download your verified datasets as CSV
2. **Prepare Data**: Format as parallel sentences (English ↔ Telugu)
3. **Choose Framework**: 
   - **HuggingFace Transformers** (Recommended for most users)
   - **IndicTrans2 Official Scripts** (Optimized for Indian languages)
   - **Custom PyTorch** (For advanced control)

4. **Fine-tuning Process**:
```python
# Example using HuggingFace
from transformers import Trainer, TrainingArguments
from datasets import Dataset

# Load your training data
train_data = Dataset.from_csv("your_training_data.csv")

# Configure training
training_args = TrainingArguments(
    output_dir="./fine_tuned_model",
    num_train_epochs=3,
    per_device_train_batch_size=8,
    save_steps=500,
    logging_steps=100,
)

# Fine-tune the model
trainer = Trainer(
    model=model,
    args=training_args,
    train_dataset=train_data,
)

trainer.train()
```

#### External API Integration
```python
# Example API integration
import requests

def translate_with_dm_translator(text):
    response = requests.post(
        "https://your-domain.com/api/translate/",
        json={"text": text},
        headers={"Authorization": "Bearer your-api-key"}
    )
    return response.json()["translated_text"]

# Convert Telugu to Anu Script format
def convert_to_anu_script(telugu_text, original_text=""):
    response = requests.post(
        "https://your-domain.com/translator/download-anu-script/",
        json={
            "telugu_text": telugu_text,
            "original_text": original_text
        },
        headers={"Content-Type": "application/json"}
    )
    return response.content  # Returns downloadable file

# Convert Telugu to Devanagari
def convert_to_devanagari(telugu_text):
    response = requests.post(
        "https://your-domain.com/translator/convert-telugu-to-devanagari/",
        data={"telugu_text": telugu_text}
    )
    return response.json()["devanagari_text"]
```

## 🔧 Troubleshooting

### Common Issues and Solutions

#### 1. Translation Problems

**Slow Translation Performance**
```bash
# Check system resources
htop
df -h

# Monitor Django logs
tail -f logs/django.log

# Check Gunicorn workers
sudo systemctl status dm_translator
```

**Poor Translation Quality**
- Verify IndicTrans2 model is properly loaded
- Check for sufficient RAM (16GB+ recommended)
- Review input text quality
- Use feedback system to report issues

**Failed File Uploads**
```bash
# Check file permissions
ls -la media/uploads/

# Check disk space
df -h

# Review upload limits in settings
grep -r "FILE_UPLOAD_MAX_MEMORY_SIZE" .
```

#### 2. Server Issues

**502 Bad Gateway**
```bash
# Check Gunicorn status
sudo systemctl status dm_translator
sudo journalctl -u dm_translator

# Check socket permissions
ls -la /run/gunicorn/

# Restart services
sudo systemctl restart dm_translator nginx
```

**Database Connection Errors**
```bash
# Test database connection
sudo -u postgres psql -d dm_translator_db -U dm_translator_user

# Check PostgreSQL status
sudo systemctl status postgresql

# Review database logs
sudo tail -f /var/log/postgresql/postgresql-*-main.log
```

**Static Files Not Loading**
```bash
# Recollect static files
python manage.py collectstatic --noinput

# Check Nginx configuration
sudo nginx -t

# Verify file permissions
ls -la static/
```

#### 3. Permission Issues

**Media File Permission Errors**
```bash
# Fix ownership
sudo chown -R www-data:www-data media/
sudo chmod -R 755 media/

# Check SELinux (if applicable)
getenforce
```

**Log File Permission Errors**
```bash
# Fix log permissions
sudo chown -R www-data:www-data logs/
sudo chmod -R 644 logs/
```

#### 4. Performance Issues

**High Memory Usage**
```bash
# Monitor memory usage
free -h
ps aux --sort=-%mem | head

# Adjust worker settings
sudo nano /etc/systemd/system/dm_translator.service
# Reduce --workers count
```

**Slow Database Queries**
```bash
# Enable query logging
# Add to settings.py:
LOGGING = {
    'loggers': {
        'django.db.backends': {
            'level': 'DEBUG',
        }
    }
}
```

### Log Analysis

#### Important Log Locations
```bash
# Application logs
tail -f /var/www/dm_translator/dm_translator/logs/django.log

# Nginx access logs
tail -f /var/log/nginx/access.log

# Nginx error logs
tail -f /var/log/nginx/error.log

# Gunicorn logs
sudo journalctl -u dm_translator -f

# PostgreSQL logs
sudo tail -f /var/log/postgresql/postgresql-*-main.log
```

#### Log Analysis Commands
```bash
# Check for errors in last 24 hours
grep -i error /var/log/nginx/error.log | grep "$(date '+%d/%b/%Y')"

# Monitor real-time translation requests
tail -f logs/django.log | grep "translation"

# Check disk usage by logs
du -sh logs/
du -sh /var/log/nginx/
```

### Emergency Procedures

#### Service Recovery
```bash
# Restart all services
sudo systemctl restart dm_translator nginx postgresql

# Reload Nginx configuration
sudo nginx -s reload

# Check service dependencies
sudo systemctl list-dependencies dm_translator
```

#### Database Recovery
```bash
# Create database backup
sudo -u postgres pg_dump dm_translator_db > backup_$(date +%Y%m%d).sql

# Restore from backup
sudo -u postgres psql dm_translator_db < backup_file.sql
```

#### System Monitoring
```bash
# Install monitoring tools
sudo apt install htop iotop nethogs

# Monitor system health
htop  # CPU and memory
iotop  # Disk I/O
nethogs  # Network usage
```

## ⚡ Performance Optimization

### Translation Performance

The system includes optimized progress tracking with minimal performance impact:

#### Performance Optimization Settings

**Changes Made:**
1. **Import Once**: Moved imports outside loops (was importing on every segment)
2. **Reduced Frequency**: Progress updates only every 5 segments instead of every segment
3. **Removed Try/Except**: Eliminated error handling overhead in tight loops
4. **Added Disable Option**: `disable_progress=True` parameter to completely skip progress tracking

**Performance Comparison:**
- **Before**: 200-250 seconds (no progress tracking)
- **With Progress**: 500-530 seconds (progress tracking every segment) ❌
- **After Optimization**: ~210-260 seconds (minimal progress overhead) ✅

#### To Test Maximum Speed:
```python
# In views_translation.py, change this line:
translated_text = translate_structured_text_to_telugu(
    extracted_text, 
    preserve_structure=True, 
    session_id=session_id, 
    disable_progress=True
)

# Instead of:
translated_text = translate_structured_text_to_telugu(
    extracted_text, 
    preserve_structure=True, 
    session_id=session_id
)
```

#### Progress Options:
1. **Full Progress** (default): Updates every 5 segments
2. **No Progress** (`disable_progress=True`): Maximum speed, no segment tracking
3. **Original Method**: Remove `session_id` parameter entirely

### Database Optimization

```bash
# PostgreSQL optimization
sudo nano /etc/postgresql/*/main/postgresql.conf

# Key settings to adjust:
shared_buffers = 256MB
effective_cache_size = 1GB
maintenance_work_mem = 64MB
checkpoint_completion_target = 0.7
wal_buffers = 16MB
default_statistics_target = 100
random_page_cost = 1.1
```

### Caching Configuration

```python
# Add to settings.py for Redis caching
CACHES = {
    'default': {
        'BACKEND': 'django_redis.cache.RedisCache',
        'LOCATION': 'redis://127.0.0.1:6379/1',
        'OPTIONS': {
            'CLIENT_CLASS': 'django_redis.client.DefaultClient',
        }
    }
}
```

### Static File Optimization

```bash
# Enable compression in Nginx
sudo nano /etc/nginx/sites-available/dm_translator

# Add to server block:
gzip on;
gzip_vary on;
gzip_min_length 1024;
gzip_types text/plain text/css application/json application/javascript text/xml application/xml;
```

### Model Performance

```python
# Optimize IndicTrans2 model loading
# In settings.py or model configuration:
INDICTRANS_CONFIG = {
    'model_cache': True,
    'batch_size': 32,
    'max_length': 512,
    'device': 'auto',  # Automatically detect GPU/CPU
}
```

### Advanced Translation Configuration

**Performance Profiles** (configurable via admin panel):
- **Speed**: num_beams=1, max_length=128, batch_size=32
- **Balanced**: num_beams=3, max_length=256, batch_size=8 (default)
- **Quality**: num_beams=5, max_length=512, batch_size=4
- **Custom**: Manual parameter control

**Translation Parameters**:
- `num_beams`: Beam search width (1-10)
- `max_length`: Maximum sequence length
- `batch_size`: Processing batch size
- `length_penalty`: Length preference (default: 1.1)
- `repetition_penalty`: Repetition avoidance (default: 1.05)
- `max_cache_size`: Translation cache limit (default: 500)

## 💾 Backup and Maintenance

### Automated Backup Script

```bash
# Create backup script
sudo nano /usr/local/bin/backup_dm_translator.sh
```

```bash
#!/bin/bash
BACKUP_DIR="/var/backups/dm_translator"
DATE=$(date +%Y%m%d_%H%M%S)

mkdir -p $BACKUP_DIR

# Database backup
sudo -u postgres pg_dump dm_translator_db > $BACKUP_DIR/db_backup_$DATE.sql

# Media files backup
tar -czf $BACKUP_DIR/media_backup_$DATE.tar.gz -C /var/www/dm_translator media/

# Application backup (excluding virtual environment)
tar -czf $BACKUP_DIR/app_backup_$DATE.tar.gz -C /var/www/dm_translator \
    --exclude='venv' --exclude='media' --exclude='logs' --exclude='.git' .

# Keep only last 7 days of backups
find $BACKUP_DIR -name "*.sql" -mtime +7 -delete
find $BACKUP_DIR -name "*.tar.gz" -mtime +7 -delete

echo "Backup completed: $DATE"
```

```bash
# Make executable
sudo chmod +x /usr/local/bin/backup_dm_translator.sh

# Add to crontab for daily backups
sudo crontab -e
# Add: 0 2 * * * /usr/local/bin/backup_dm_translator.sh
```

### Update Procedures

```bash
# Application updates
cd /var/www/dm_translator/dm_translator
git pull origin main
source venv/bin/activate
pip install -r requirements.txt --upgrade
python manage.py migrate
python manage.py collectstatic --noinput
sudo systemctl restart dm_translator

# System updates
sudo apt update && sudo apt upgrade -y
sudo systemctl restart nginx
```

### Monitoring Setup

```bash
# Install monitoring tools
sudo apt install htop iotop sysstat

# Monitor system resources
watch -n 1 'free -h && df -h'

# Check service status regularly
systemctl status dm_translator nginx postgresql
```

## 🤝 Support & Contributing

### Getting Help

#### Documentation
- **GitHub Repository**: https://github.com/dmouli408/DM_Translator
- **Issues**: Report bugs and request features
- **Discussions**: Community support and questions

#### Log Analysis
- **Application Logs**: `/var/www/dm_translator/dm_translator/logs/django.log`
- **System Logs**: `sudo journalctl -u dm_translator`
- **Error Tracking**: Built-in Django error reporting

#### Community Support
- **GitHub Issues**: Technical problems and bug reports
- **Discussions**: Usage questions and feature requests
- **Wiki**: Additional documentation and tutorials

### Contributing

#### Bug Reports
1. Check existing issues first
2. Provide detailed reproduction steps
3. Include system information and logs
4. Use issue templates when available

#### Feature Requests
1. Describe the use case clearly
2. Explain expected behavior
3. Consider backward compatibility
4. Provide mockups or examples if applicable

#### Code Contributions
1. Fork the repository
2. Create a feature branch
3. Follow coding standards
4. Write tests for new features
5. Update documentation
6. Submit a pull request

### Development Setup

```bash
# Clone for development
git clone https://github.com/dmouli408/DM_Translator.git
cd DM_Translator/dm_translator

# Install development dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt  # If available

# Run tests
python manage.py test

# Code quality checks
flake8 .
black .
isort .
```

### License

This project is licensed under the MIT License - see the LICENSE file for details.

### Acknowledgments

- **AI4Bharat** for the IndicTrans2 model
- **Django Community** for the excellent framework
- **Bootstrap** for the UI components
- **Contributors** who help improve this project

---

**📧 Contact**: For urgent issues or private inquiries, contact the maintainers through GitHub.

**🌟 Star the Project**: If DM Translator helps you, please star the repository to support development!

**🔄 Stay Updated**: Watch the repository for new releases and updates.

---

## 🌟 Star this project if it helped you!
[![GitHub stars](https://img.shields.io/github/stars/dmouli408/DM_Translator.svg?style=social&label=Star)](https://github.com/dmouli408/DM_Translator)
[![GitHub forks](https://img.shields.io/github/forks/dmouli408/DM_Translator.svg?style=social&label=Fork)](https://github.com/dmouli408/DM_Translator)

## Made with ❤️ by Dasari Mouli
**Panchayat Secretary Gr-VI (Digital Assistant)**  
Edupugallu-2 Secretariat, Kankipadu Mandal, Krishna District

*This project was developed independently as a personal initiative to provide quality AI-powered English to Telugu translation services.*
