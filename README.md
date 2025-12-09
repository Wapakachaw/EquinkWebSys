EquInk/
│
├── backend/
│   ├── app.py              # Flask server & API endpoints
│   ├── database.py         # SQLite database operations
│   └── requirements.txt    # Python dependencies
│
├── frontend/
│   ├── index.html          # File upload page
│   ├── breakdown.html      # Cost breakdown & pricing page
│   ├── admin.html          # Analytics dashboard
│   ├── css/
│   │   └── style.css       # Monochrome styling
│   └── js/
│       ├── upload.js       # Upload handling
│       ├── breakdown.js    # Cost calculations
│       └── admin.js        # Dashboard charts
│
└── database/
    └── equink.db           # SQLite database (auto-generated)

🔧 Prerequisites
Before installing, ensure you have:

Python 3.8 or higher
pip (Python package manager)
Poppler (for PDF to image conversion)
Modern web browser (Chrome, Firefox, Edge)

EquInk - Automated Printing Cost and Management System
A smart, data-driven solution for print-shop operations that automatically calculates printing costs based on ink usage detection.
Show Image
Show Image
Show Image

📋 Features

Intelligent Ink Detection: Analyzes PDF/DOCX files using image processing to accurately detect black and colored ink percentages
Dynamic Pricing: Adjustable pricing rates per ink percentage
Printer Management: Track and select from multiple printers
Analytics Dashboard:

Hotspot time analysis (orders by hour)
Monthly sales tracking
Weekly revenue reports
Printer usage statistics


Order History: Complete database of all print jobs with timestamps
Responsive UI: Clean, monochrome design with collapsible sections


🗂️ Project Structure
EquInk/
│
├── backend/
│   ├── app.py              # Flask server & API endpoints
│   ├── database.py         # SQLite database operations
│   └── requirements.txt    # Python dependencies
│
├── frontend/
│   ├── index.html          # File upload page
│   ├── breakdown.html      # Cost breakdown & pricing page
│   ├── admin.html          # Analytics dashboard
│   ├── css/
│   │   └── style.css       # Monochrome styling
│   └── js/
│       ├── upload.js       # Upload handling
│       ├── breakdown.js    # Cost calculations
│       └── admin.js        # Dashboard charts
│
└── database/
    └── equink.db           # SQLite database (auto-generated)

🔧 Prerequisites
Before installing, ensure you have:

Python 3.8 or higher
pip (Python package manager)
Poppler (for PDF to image conversion)
Modern web browser (Chrome, Firefox, Edge)


📦 Installation
Step 1: Clone or Download the Project
bash# Create project directory
mkdir EquInk
cd EquInk
Step 2: Install Poppler (Required for PDF Analysis)
Windows:

Download Poppler from: https://github.com/oschwartz10612/poppler-windows/releases
Extract to C:\poppler-25.11.0\ (or any location)
Note the path to the bin folder (e.g., C:\poppler-25.11.0\bin)

macOS:
bashbrew install poppler
Linux (Ubuntu/Debian):
bashsudo apt-get install poppler-utils
Step 3: Install Python Dependencies
bashcd backend

# Create virtual environment (recommended)
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install all required packages
pip install -r requirements.txt
Step 4: Configure Poppler Path
Edit backend/app.py line 16:
pythonPOPPLER_PATH = r"C:\poppler-25.11.0\bin"  # Update this to YOUR Poppler path

📚 Required Python Packages
Create a requirements.txt file in the backend/ folder with:
txtflask==3.0.0
flask-cors==4.0.0
PyPDF2==3.0.1
python-docx==1.1.0
pillow==10.4.0
pdf2image==1.16.3
opencv-python==4.8.1.78
numpy==1.24.3
Or install directly:
bashpip install flask flask-cors PyPDF2 python-docx pillow pdf2image opencv-python numpy

🚀 Running the Application
Terminal 1: Start Backend Server
bashcd backend
python app.py
Expected output:
 * Running on http://127.0.0.1:5000
 * Debug mode: on
Terminal 2: Start Frontend Server
bashcd frontend
python -m http.server 8000
Expected output:
Serving HTTP on 0.0.0.0 port 8000
Access the Application
Open your browser and navigate to:
http://localhost:8000

💡 Usage Guide
1. Upload Documents

Drag & drop or select PDF/DOCX files
Supported formats: .pdf, .docx
Files are automatically analyzed for ink usage

2. Review Breakdown

View per-page ink percentages
Adjust pricing rates (₱ per %)
Select printer for the job
Review total cost before confirming

3. Admin Dashboard

View order history
Analyze peak printing times
Track monthly sales and revenue
Monitor printer usage statistics


