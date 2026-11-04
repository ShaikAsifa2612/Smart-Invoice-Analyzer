# Smart Invoice Analyzer

An intelligent invoice processing system that extracts data from **multilingual invoices** using OCR and NLP, and flags suspicious invoices with a **machine learning fraud detection model**. Results are shown in an interactive **Streamlit** dashboard.



> This was a **group project**. See [Team and My Contribution](#team-and-my-contribution) below.



## Features

- **OCR extraction:** reads text from invoice images and scanned documents
- **Multilingual support:** works with invoices written in different languages
- **NLP-based field extraction:** picks out key details such as invoice number, date, vendor and amounts
- **Fraud detection:** a Random Forest classifier flags invoices that look suspicious
- **Handles class imbalance:** fraudulent invoices are rare, so the model is evaluated with precision and recall, not just accuracy
- **Interactive dashboard:** upload an invoice and see the extracted data and fraud analysis in Streamlit

## Tech Stack

| Area | Technologies |
| ---- | ------------ |
| Language | Python |
| Text extraction | OCR |
| Language processing | NLP |
| Machine learning | scikit-learn (RandomForestClassifier), Pandas, NumPy |
| Dashboard | Streamlit |

## How It Works

1. **Upload:** the user uploads an invoice image or document in the dashboard.
2. **OCR:** text is extracted from the invoice.
3. **NLP:** key fields are identified and cleaned from the extracted text.
4. **Fraud check:** the extracted features go into the trained Random Forest model.
5. **Result:** the dashboard shows the extracted data along with the fraud prediction.

## Project Structure

```
Smart-Invoice-Analyzer/
├── app.py                  (Streamlit dashboard)
├── requirements.txt        (Python dependencies)
├── model/                  (trained fraud detection model)
├── data/                   (sample invoices and datasets)
├── assets/                 (screenshots)
└── README.md
```

> Update this tree to match your actual folders and file names.

## Getting Started

### Prerequisites

- Python 3.9 or higher
- pip

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/ShaikAsifa2612/Smart-Invoice-Analyzer.git
   cd Smart-Invoice-Analyzer
   ```

2. (Optional) Create a virtual environment:

   ```bash
   python -m venv venv
   venv\Scripts\activate        # Windows
   source venv/bin/activate     # macOS / Linux
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the app:

   ```bash
   streamlit run app.py
   ```

5. Open the link shown in the terminal, usually `http://localhost:8501`.

> The OCR step may need an extra tool installed on your system. Add the setup steps here if your project requires one.

## Fraud Detection Model

- **Algorithm:** Random Forest Classifier (scikit-learn)
- **Challenge:** class imbalance, because genuine invoices far outnumber fraudulent ones
- **Evaluation:** precision and recall, which show how many frauds are caught and how many alerts are correct


## Team and My Contribution

This project was built by a team of students.

| Member | Contribution |
| ------ | ------------ |
| **Shaik Asifa** | Built and trained the **fraud detection model** (Random Forest), handled class imbalance, and evaluated it with precision and recall |
| Mohan | Dashboard |
| Lalitha | Streamlit  |

## Future Improvements

- Support more languages and invoice layouts
- Add more fraud signals and a larger training dataset
- Export results to CSV or Excel
- Deploy the app online with a shareable link

## Author

**Shaik Asifa**

- GitHub: [ShaikAsifa2612](https://github.com/ShaikAsifa2612)
- LinkedIn: [sk-asifa-888a6322b](www.linkedin.com/in/shaik-asifa2612)
- Email: skasifa2612@gmail.com
