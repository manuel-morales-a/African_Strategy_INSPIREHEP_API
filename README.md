# African Strategy – INSPIRE-HEP API Tools

This repository aims to provide an accessible and reproducible workflow for exploring scientific activity in **High Energy, Cosmology, and Astroparticle Physics (HECAP)** across Africa using the **INSPIRE-HEP API**. It is designed to help students, researchers, and science-policy teams quickly gather publication information in a transparent and open way.

The included Jupyter Notebook demonstrates how to retrieve and analyse records (specifically author information) associated with African institutions. As a concrete example, we explore HECAP metrics for **Nigeria**, but the same approach can be applied to any country in the region.

> **Note:**  
> This analysis is intentionally simplified, quick, and built for outreach and exploratory use.  
> It is not a full scientometric pipeline, and bugs or missing edge cases should be expected.  
> The goal is to provide a clear, minimal workflow that anyone can adapt and improve!

This project aims to support outreach and community-building by providing a simple way to explore HECAP activity across Africa. The goal is to offer a transparent starting point that can inform discussions about the development and support of HECAP in the region.

The workflow follows the methodology used in **_Statistical Analysis of Scientific Metrics in High Energy, Cosmology, and Astroparticle Physics in Latin America_**, an open scientometric study whose INSPIRE-HEP record is available here: https://inspirehep.net/literature/2897923.

Have fun! 

---

## 📁 Repository Structure

```
African_Strategy_INSPIREHEP_API/
│
├── main.ipynb               # Main notebook demonstrating API usage
├── data/                    # Optional data folder (results, cached queries, etc.)
├── environment.yml          # Reproducible Conda environment
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

- `requests` → for HTTP queries to the INSPIRE API  
- `json` → part of the Python standard library  

These are already included in `environment.yml`.

---

## 📡 Data

The `data/` directory contains small example files used by the notebook.  
All data can be **easily regenerated** from the INSPIRE-HEP API.

### Nigeria example (`nigeria_api.json`)

The file `nigeria_api.json` contains the list of **Nigerian institutions** returned by the INSPIRE-HEP **institutions** endpoint. It was generated using a country query of the form:

```
https://inspirehep.net/api/institutions?q=nigeria
```

From this result, we select institutions with `number_of_papers > 0` and extract their `legacy_ICN` codes.  
These codes are then used to retrieve the associated authors of Nigeria and their collaborators, which form the basis of the example analysis in the notebook `main.ipynb`, which you are welcome to run.

The same procedure can be applied to **any other country of interest** by replacing `nigeria` in the query.

### Notes

The folder may also include:
- cached JSON results,
- small processed tables,
- temporary outputs.

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

## 📄 License

You are free to use, modify, and distribute it.

