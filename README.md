# African Strategy – INSPIRE-HEP API Tools

This repository contains a simple and reproducible workflow to query the **INSPIRE-HEP API** and extract publication metadata related to African institutions. It includes a Jupyter Notebook demonstrating the workflow, together with minimal code and data files designed to help researchers replicate or extend the analysis.

The project is lightweight and suitable for anyone interested in scientometrics, HEP outreach, or automated retrieval of publication information from INSPIRE-HEP.

---

## 📁 Repository Structure

```
African_Strategy_INSPIREHEP_API/
│
├── main.ipynb               # Main notebook demonstrating API usage
├── data/                    # Optional data folder (results, cached queries, etc.)
├── environment.yml          # Reproducible Conda environment
├── requirements.txt         # Minimal pip-based environment (optional alternative)
├── .gitignore               # Standard ignore rules
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

You can reproduce the notebook environment using Conda (recommended) or pip.

### **Option A — Using Conda**

```bash
conda env create -f environment.yml
conda activate african-strategy
```

### **Option B — Using pip**

```bash
python -m venv .venv
source .venv/bin/activate      # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

---

## 📊 Running the Notebook

Start Jupyter and open the main notebook:

```bash
jupyter notebook
```

Then open:

```
main.ipynb
```

and run all cells.

---

## 🧰 Dependencies

The project uses only three libraries:

- `IPython` → to display formatted API outputs  
- `requests` → for HTTP queries to the INSPIRE API  
- `json` → part of the Python standard library  

These are already included in `environment.yml` or `requirements.txt`.

---

## 📡 Data

The `data/` directory is included for convenience and may contain:

- cached JSON results from API calls  
- processed data tables  
- temporary output files  

If you plan to store **large** datasets, consider adding them to `.gitignore`.

---

## 📘 Purpose

This repository was created to support work on:

- Scientometrics in Africa  
- INSPIRE-HEP data exploration  
- Automated publication retrieval  
- HEP outreach and regional strategy studies  

You are welcome to fork or extend this project for similar research or for educational purposes.

---

## 🔧 Customisation

Feel free to modify:

- the notebook to include additional fields, queries, or visualisation  
- the data folder structure  
- the query logic (e.g., search for countries, collaborations, authors, or topics)

If you want, I can help you turn this into a small **Python package** (e.g., `inspire_africa`) with functions and CLI commands.

---

## 📄 License

The project is released under the MIT License.  
You are free to use, modify, and distribute it.

