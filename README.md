
# 📜 AI-Powered Contract Compliance Checker

An end-to-end AI system that automatically analyzes contract PDFs, extracts legal clauses, evaluates regulatory risks, detects compliance gaps, and generates actionable compliance insights. It also supports notifications (Slack/Email) and reporting via Google Sheets.

---

## 🚀 Features

✅ Upload Contract PDF via Streamlit UI  
✅ Extract & normalize contract text  
✅ Clause extraction (LLM based + fallback extraction)  
✅ Risk scoring per clause using LLM (Groq/OpenRouter)  
✅ Compliance gap analysis (GDPR / HIPAA)  
✅ Live regulatory update tracking (RSS + scraping fallback)  
✅ Slack alerts for compliance issues  
✅ Email notifications for high severity alerts  
✅ Google Sheets reporting (Contracts Overview, Issues, Audit log)  
✅ Exports: CSV + JSON for annotations & results  

---

## 🧠 Architecture / Pipeline Flow

1. **PDF Text Extraction**
2. **Text Cleaning & Normalization**
3. **Clause Extraction**
4. **LLM-based Risk Assessment**
5. **Live Regulatory Updates**
6. **Compliance Gap Analysis**
7. **Reporting + Alerts**
   - Slack Notification
   - Email Notification
   - Google Sheets Update
8. **Outputs**
   - JSON report
   - CSV annotations

---

## 🛠 Tech Stack

- **Python**
- **Streamlit** (UI)
- **Groq LLM API**
- **OpenRouter** (optional fallback)
- **Google Sheets API (gspread)**
- **Slack Webhooks**
- **SMTP Email (Gmail App Password)**
- **Pandas / JSON / CSV utilities**

---

## 📂 Project Structure

```bash
ai_code/
│── app.py
│── run.py
│── requirements.txt
│── .env.example
│── credentials/
│   └── service_account.json   # (ignored in git)
│── data/
│   ├── raw/
│   └── processed/
│── annotations/
│── src/
│   ├── clause_engine/
│   ├── risk_engine/
│   ├── integrations/
│   │   ├── google_sheets/
│   │   ├── email_notifier.py
│   │   ├── slack_notifier.py
│   ├── regulatory/
│   └── utils/
