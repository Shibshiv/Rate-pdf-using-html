# ✨ Rate-pdf-using-html

<p align="center">
  <img src="https://img.shields.io/badge/status-active-success?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/language-HTML%20%7C%20JavaScript-informational?style=for-the-badge" alt="Language" />
  <img src="https://img.shields.io/badge/license-MIT-blue?style=for-the-badge" alt="License" />
</p>

<p align="center">
  A sleek, browser-based PDF library rater that analyzes local PDF files and scores them using simple, transparent heuristics.
</p>

---

## 🌟 Overview

**Rate-pdf-using-html** is a lightweight, client-side PDF analysis tool built with **HTML**, **JavaScript**, and **PDF.js**.

It allows you to select a folder of PDFs from your device, extract text directly in the browser, and generate a rating for each file based on document structure and content signals.

Perfect for quick library checks, school projects, and simple PDF triage workflows.

---

## 🚀 Key Features

- 📂 Select a local folder containing PDF files
- 🔍 Extract text from each PDF in the browser
- 📊 Generate a rating for each document
- 🧠 Use simple heuristics based on pages, words, and keywords
- 🖥️ View results instantly in a clean table
- 🔒 Runs entirely client-side — no server required

---

## ⚙️ How It Works

The app uses [`pdf.js`](https://cdnjs.cloudflare.com/ajax/libs/pdf.js/) to process PDF files locally in the browser.

### Workflow

1. Open the page in a modern browser
2. Click **Choose Folder**
3. Select a directory containing PDF files
4. The app extracts text from each document
5. A score from `0` to `100` is calculated
6. Results are displayed in a structured table

---

## 🧮 Scoring Logic

The rating is intentionally simple and easy to understand:

- **Page count** contributes up to 40 points
- **Word count** contributes up to 25 points
- **Keyword matches** add points for terms such as:
  - `introduction`
  - `chapter`
  - `summary`
  - `reference`
  - `exercise`
- Final score is capped at **100**

> This rating is designed for quick comparison, not academic or production-grade assessment.

---

## 📁 Project Structure

- `PDF_Library_Rater.html` — main application file
- `README.md` — project documentation
- `LICENSE` — MIT License

---

## 🛠️ Requirements

- A modern browser with support for the **File System Access API**
- Internet access to load **PDF.js** from the CDN

---

## ▶️ Usage

1. Open `PDF_Library_Rater.html` in your browser.
2. Click **Choose Folder**.
3. Pick a folder containing `.pdf` files.
4. Review the pages, word counts, scores, and explanations.

---

## ⚠️ Notes

- For privacy and security reasons, browsers cannot scan your entire device automatically.
- You must manually choose the folder you want to analyze.
- This project uses a heuristic approach, so scores are approximate.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Made with ❤️ for simple PDF analysis.
</p>
