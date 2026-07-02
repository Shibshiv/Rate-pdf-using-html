# Rate-pdf-using-html

A simple browser-based PDF library rater built with HTML, JavaScript, and PDF.js.

## Overview

This project lets you choose a folder of PDF files from your computer and generates a basic rating for each file based on simple heuristics such as:

- number of pages
- estimated word count
- presence of common structural keywords like `introduction`, `chapter`, `summary`, `reference`, and `exercise`

The results are displayed in a table directly in the browser.

## Features

- Select a local folder containing PDF files
- Extract text from each PDF in the browser
- Rate PDFs using a simple scoring system
- Display page count, word count, rating, and reasoning
- Runs entirely client-side

## How it works

The app uses [`pdf.js`](https://cdnjs.cloudflare.com/ajax/libs/pdf.js/) to read PDF files in the browser. For each PDF:

1. The browser opens a folder picker
2. Each `.pdf` file in the selected folder is processed
3. Text is extracted from all pages
4. A heuristic score from `0` to `100` is calculated
5. The results are shown in a table

## Scoring logic

The rating is based on a simple heuristic:

- up to 40 points for page count
- up to 25 points for word count
- 5 points for each matched keyword
- final score is capped at 100

This means the score is only a rough estimate and is best suited for quick comparisons rather than formal evaluation.

## Project structure

- `PDF_Library_Rater.html` — main app file
- `README.md` — project documentation
- `LICENSE` — MIT license

## Usage

1. Open `PDF_Library_Rater.html` in a browser.
2. Click **Choose Folder**.
3. Select a folder that contains PDF files.
4. View the extracted statistics and ratings in the table.

## Requirements

- A modern browser that supports the File System Access API
- Internet access to load `pdf.js` from the CDN

## Notes

- Browser security prevents automatic scanning of your whole computer; you must manually choose a folder.
- This project is a student project and uses a lightweight heuristic rather than machine learning.

## License

This project is licensed under the MIT License. See `LICENSE` for details.
