# 🕵️ FORENSIS-AI - UFDR Triage MVP

A digital forensics AI platform for analyzing Universal Forensic Data Reports (UFDR) with behavioral intelligence, pattern detection, and automated triage capabilities.

## 🎯 Overview

FORENSIS-AI is an intelligent forensic analysis tool designed to help investigators quickly triage and analyze communication data from UFDR JSON files. It combines vector-based semantic search, behavioral pattern analysis, and AI-powered insights to identify suspicious activities, financial transactions, and communication anomalies.

## ✨ Key Features

### 🔍 Forensic Analysis
- **Automated Triage**: AI-powered analysis of UFDR data to identify suspicious communications, financial activity, and unusual patterns
- **Manual Query Interface**: Natural language search across messages with entity highlighting
- **Entity Recognition**: Automatic detection and highlighting of crypto addresses, phone numbers, bank details, and financial amounts
- **Multi-language Support**: Auto-detection and translation of messages in Tamil, Hindi, Bengali, Telugu, and Marathi

### 🧠 Behavioral Intelligence
- **Temporal Anomaly Detection**: Identifies unusual messaging patterns (1-4 AM activity, message spikes)
- **Contact Pattern Analysis**: Tracks new contacts, contact drops, and relationship changes
- **Interactive Visualizations**: Timeline charts and network graphs for communication patterns
- **AI Investigative Suggestions**: Context-aware recommendations for next investigative steps

### 📊 Reporting & Export
- **PDF Report Generation**: Professional forensic reports with findings, metadata, and behavioral insights
- **Chain of Custody Logging**: Tracks all actions and maintains integrity verification
- **Downloadable Results**: Export analysis results for further investigation

## 🚀 Getting Started

### Prerequisites

```bash
Python 3.8+
pip (Python package manager)
```

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd forensis-ai
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Set up environment variables**
```bash
# Create a .env file in the project root
echo "GEMINI_API_KEY=your_api_key_here" > .env
```

4. **Run the application**
```bash
streamlit run frontend/app.py
```

The app will open in your browser at `http://localhost:8501`

## 📁 Project Structure

```
forensis-ai/
├── frontend/
│   ├── app.py                 # Main Streamlit application
│   └── chroma_db/            # Vector database storage
├── backend/
│   ├── ingest.py             # UFDR data ingestion
│   └── search_engine.py      # Hybrid search implementation
├── utils/
│   ├── highlighter.py        # Entity highlighting & text cleaning
│   ├── pdf_generator.py      # PDF report generation
│   ├── chain_of_custody.py   # Audit logging
│   ├── anomaly_detection.py  # Behavioral analysis
│   ├── gemini_client.py      # AI client integration
│   └── translation.py        # Multi-language support
├── data/
│   └── sample_ufdr.json      # Sample data file
└── requirements.txt          # Python dependencies
```

## 📖 Usage Guide

### 1. Upload Data
- Click **"Upload UFDR Data"** and select your JSON file, or
- Click **"Load Sample Data"** to try the demo

### 2. Run Behavioral Analysis
- Click **"🔊 Run Behavioral Analysis"** to detect:
  - Unusual messaging times (1-4 AM)
  - Message volume spikes
  - New contacts within 24 hours
  - Contact pattern disruptions
  - Communication network visualization

### 3. Forensic Analysis
- **Automated Analysis**: Click **"🔎 Run Automated Forensic Analysis"** for AI-powered triage
- **Manual Search**: Enter queries like:
  - "Show me crypto addresses"
  - "Find suspicious activity"
  - "Messages with financial transactions"

### 4. Review Results
- Explore highlighted entities (crypto wallets, phone numbers, amounts)
- View temporal patterns and contact networks
- Read AI investigative suggestions

### 5. Export Report
- Click **"📥 Export to PDF"** to download a comprehensive forensic report

## 🔧 Configuration

### UFDR JSON Format

```json
{
  "messages": [
    {
      "message_id": "msg_001",
      "timestamp": "2025-01-15T14:30:00Z",
      "sender": "user@example.com",
      "recipient": "contact@example.com",
      "content": "Message text here",
      "media_path": "optional/path/to/media.jpg"
    }
  ],
  "chain_of_custody": [],
  "media_analysis": [],
  "evidence_highlights": [],
  "manifest": {}
}
```

### Supported Languages
- English (en)
- Tamil (ta)
- Hindi (hi)
- Bengali (bn)
- Telugu (te)
- Marathi (mr)
- Auto-detection enabled by default

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **Vector Database**: ChromaDB
- **AI/ML**: Google Gemini API
- **NLP**: spaCy, langdetect
- **Visualization**: Plotly, NetworkX
- **PDF Generation**: ReportLab

## 🔒 Security & Privacy

- All data processing happens locally
- No data is sent to external services (except Google Translate API for translation)
- Chain of custody logging for audit trails
- Integrity verification for evidence handling

## 📊 Key Metrics Detected

- **Financial Indicators**: Crypto addresses, bank details, transaction amounts
- **Contact Patterns**: New relationships, dropped contacts, frequency changes
- **Temporal Anomalies**: Odd-hour activity (1-4 AM), message spikes
- **Behavioral Flags**: Suspicious keywords, coordination patterns, urgency indicators

## 👥 Authors

**DIVYESH HARI G**  
📧 divyesh02208@gmail.com  
🔗 [github.com/DIVYESH-HARI](https://github.com/DIVYESH-HARI)

**G.K.AKASHGAUTHAM**  
📧 gkakash2006@gmail.com  
🔗 [github.com/Akashgautham](https://github.com/Akashgautham)

**K.RAKSHITHASRI**  
📧 rakshiekt@gmail.com  
🔗 [github.com/rakshithasri06](https://github.com/rakshithasri06)

**VIJAYA KARTHICK RAJA U M**  
📧 vkr3056@gmail.com  
🔗 [github.com/KARTHICK-3056](https://github.com/KARTHICK-3056)

**S.S.MADHAVAN**  
📧 ssmadhavan006@gmail.com  
🔗 [github.com/ssmadhavan006](https://github.com/ssmadhavan006)

**M.N.RAKSHA**  
📧 rakshanathan006@gmail.com  
🔗 [github.com/raksha006](https://github.com/raksha006)

## 🙏 Acknowledgments

Built for digital forensics professionals to accelerate investigation workflows and improve evidence analysis.

---

**⚠️ Disclaimer**: This tool is designed for legitimate forensic investigation purposes only. Users are responsible for ensuring compliance with applicable laws and regulations.
