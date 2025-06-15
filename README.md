# AI-Risk-Assessment

A lightweight Python tool to extract and analyze **SOC 2 audit reports** (or other compliance-related documents in PDF format) for **risk indicators** and **technical framework segments** such as ports, APIs, and modules.

---

## 🚀 Features

* 📄 **PDF Parsing** using `PyMuPDF`
* 🧠 **NLP with spaCy** to process and analyze content
* ⚠️ **Risk Indicator Detection**

  * Third-party data sharing
  * Log retention practices
  * Source code review references
* 🔍 **Framework Segment Extraction**

  * Port mentions (`port 80`, `port 443`, etc.)
  * APIs and Modules references via regex
* ✅ Terminal-based result summary

---

## 🧰 Requirements

Make sure the following Python packages are installed:

```bash
pip install spacy PyMuPDF fpdf
python -m spacy download en_core_web_sm
```

---

## 📂 File Structure

```
SOC2-PDF-Analyzer/
├── sample_soc2_report.pdf      # Your input SOC 2 report
├── analyzer.py                 # The main analysis script
└── README.md                   # You're reading this!
```

---

## 💻 Usage

```bash
python analyzer.py
```

Make sure to place your target SOC 2 PDF at the path specified inside `analyzer.py` (default: `/content/sample_soc2_report.pdf`).

---

## 🧪 Sample Output

```
📄 Reading PDF: /content/sample_soc2_report.pdf

📊 RISK INDICATORS:
  - Third Party Data Sharing: ✅ Detected
  - Log Retention: ✅ Detected
  - Source Code Review: ✅ Detected

🔍 FRAMEWORK SEGMENTS:
  - Ports: port 22, port 443
  - Apis: APIs, API
  - Modules: modules, Modules, Module
```

---

## 🧠 How It Works

* **Risk Indicators** are identified via simple keyword matching after lowercasing and tokenization with `spaCy`.
* **Framework Segments** are extracted using pre-defined regular expressions.

---

## 🔒 Ideal For

* SOC 2 Audit Report Pre-analysis
* Compliance Document Review
* Security Report Processing Pipelines

---

## 📌 Future Improvements

* Add support for other compliance types (ISO 27001, NIST 800-53, etc.)
* Expand risk indicators with customizable dictionaries
* Add PDF summary export using `fpdf`

---
