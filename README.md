# CSCN8040-VTrack Project

## Group Members
- Shantanu Dixit — 8965610  
- Serageldin Monir Farid Abdelghaffar Abdelmoaty — 9052380  
- Tai Siang Huang — 9006413  
- Jaiminiben Natvarbhai Rathod — 8941937  
- Mohammed Adeen Shaik — 8969152  

---

## Overview
This repository contains the **Exploratory Data Analysis (EDA)**, statistical testing, and hypothesis evaluation for the CSCN8040-VTrack project, focusing on optimizing traffic stop durations using AI-assisted tools, such as a proposed RAG-based system.  
All analysis steps are performed within a single Jupyter Notebook for reproducibility.

---

## Dataset
- **Source**: Washington DC Stop Data  
- **Description**: Contains stop data from the Metropolitan Police Department (MPD) in Washington, D.C., covering vehicle, pedestrian, bicycle, and harbor stops from January 1, 2023, to June 30, 2024. Includes details like stop location, reason, duration, and outcomes (e.g., tickets, searches, arrests).

---

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/shantanudxt/CSCN8040-VTrack.git
cd CSCN8040-VTrack
```

### 2. Create and Activate a Virtual Environment
```bash
python -m venv venv
```
**Windows**
```bash
venv\Scripts\activate
```
**Mac/Linux**
```bash
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r config/requirements.txt
```

---

## Running the Analysis
The entire analysis is contained in the following notebook:  
```
notebooks/V-Track_EDA_Final.ipynb
```

To run it:
```bash
cd notebooks
jupyter notebook "V-Track_EDA_Final.ipynb"
```

---

## Notes
- All paths in the code use **relative references** for portability.  
- Ensure required data files are placed in the correct directories as referenced in the notebook.  
- Output files and visualizations are generated during notebook execution.  
