# InvoiceNet - Replit Setup

## Overview
InvoiceNet is a deep neural network application for extracting intelligent information from invoice documents. This project has been successfully imported and configured for the Replit environment.

## Project Status
- **Status**: ✅ Successfully imported and configured
- **Environment**: Replit with Python 3.11
- **Web Interface**: Running on port 5000
- **Deployment**: Configured for autoscale

## Architecture
This is a Python-based machine learning application with both GUI and CLI interfaces:

### Core Components
- **GUI Applications**: Tkinter-based extractor and trainer interfaces
- **CLI Tools**: Command-line tools for data preparation, training, and prediction
- **Web Interface**: Static HTML interface showing project status and usage
- **ML Models**: TensorFlow-based deep learning models for information extraction

### Key Files
- `extractor.py` - GUI for extracting information from invoices
- `trainer.py` - GUI for training custom models
- `predict.py` - CLI tool for invoice prediction
- `train.py` - CLI tool for model training
- `prepare_data.py` - Data preparation utility
- `setup.py` - Package configuration with dependencies
- `index.html` - Web interface landing page

## Features
### Supported Invoice Fields
- **General**: Vendor name, invoice number, customer info
- **Amounts**: Total amount, tax amount, subtotal
- **Dates**: Invoice date, due date, service date  
- **Optional**: Custom configurable fields

### Interfaces Available
1. **Web Interface** (Port 5000): Status page and documentation
2. **GUI Applications**: Tkinter-based extractor and trainer
3. **CLI Tools**: Command-line automation tools

## Dependencies
### System Dependencies (Installed)
- Python 3.11
- Tesseract OCR
- ImageMagick
- Ghostscript
- Poppler

### Python Dependencies (In setup.py)
- TensorFlow 2.13.1
- NumPy
- OpenCV
- PyTesseract
- PDF processing libraries (PyPDF2, pdfplumber, pdf2image)
- Other ML and utility libraries

## Usage
### Web Interface
- Access at http://0.0.0.0:5000 
- Shows project status and usage instructions

### GUI Applications
```bash
# Launch invoice extractor GUI
python extractor.py

# Launch model trainer GUI  
python trainer.py
```

### CLI Tools
```bash
# Prepare training data
python prepare_data.py --data_dir train_data/

# Train a model
python train.py --field total_amount --batch_size 8

# Extract information from invoices
python predict.py --field total_amount --invoice file.pdf
```

## Configuration
### Workflow
- **Name**: Server
- **Command**: `python3 -m http.server 5000 --bind 0.0.0.0`
- **Port**: 5000
- **Output**: Webview

### Deployment
- **Target**: Autoscale (stateless web application)
- **Command**: `python3 -m http.server 5000 --bind 0.0.0.0`

## Recent Changes
- **2025-09-07**: Initial import and Replit environment setup
- **2025-09-07**: Created web interface and configured workflows
- **2025-09-07**: Set up deployment configuration for production

## Notes
- Full ML functionality requires installing dependencies with `pip install -e .`
- GPU acceleration available with CUDA support
- Disk space may be limited - consider lightweight deployment for web interface only
- GUI applications require X11 forwarding or VNC for remote access