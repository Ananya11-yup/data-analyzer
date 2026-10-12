# Data Analyzer

An interactive data analysis application that helps users import datasets, explore data, generate visualizations, 
discover relationships, and experiment with machine learning — all through a web-based interface.
<img width="1907" height="907" alt="image" src="https://github.com/user-attachments/assets/b2a5f9b9-c403-4053-920d-5525de4cc4a1" />
<img width="1501" height="687" alt="image" src="https://github.com/user-attachments/assets/c7443b76-aec4-4cc0-9fcd-1acc8cf94893" />
<img width="1477" height="527" alt="image" src="https://github.com/user-attachments/assets/52fbc155-833e-488a-b6ef-41591e28bfc7" />

## Table of Contents

## Overview

Data Analyzer is a Python-based data exploration project with two interfaces:

1. **Streamlit interface** — a Python-powered application for interactive analysis and dashboards.
2. **FastAPI web interface** — a backend API paired with a JavaScript frontend.

The application is designed to make common data analysis tasks easier to explore without manually writing code for every operation.

## Features

- **Data import:** Upload supported files, paste tabular data, or retrieve tables from eligible web pages.
- **Data exploration:** Search, sort, inspect, and navigate tabular data.
- **Statistical analysis:** Generate summary statistics and explore dataset characteristics.
- **Data visualization:** Create interactive charts and dashboards.
- **Correlation analysis:** Investigate relationships between numerical variables.
- **Machine learning experiments:** Explore supported prediction, clustering, and anomaly-detection workflows.
- **Reports and insights:** Review analysis results through the available reporting interface.
- **Automated testing:** Run backend tests to help verify application behavior.

Available operations depend on the input format, data quality, and the selected workflow.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Pandas | Data manipulation and analysis |
| FastAPI | Backend API |
| Streamlit | Python-based user interface |
| JavaScript, HTML, CSS | Web frontend |
| Plotly | Interactive charts and dashboards |
| Matplotlib and Seaborn | Data visualization |
| Scikit-learn | Machine learning workflows |
| Beautiful Soup and Requests | Web data retrieval and parsing |
| Pytest | Automated testing |

## Project Structure

```text
data-analyzer/
├── streamlit_app.py
├── dashboard_pro.py
├── make_password.py
├── run_website.bat
├── run_website.sh
├── start.bat
├── stop.bat
├── backend/
│   ├── main.py
│   ├── analysis.py
│   ├── charts.py
│   ├── config.py
│   ├── ml.py
│   ├── parsing.py
│   ├── store.py
│   ├── netguard.py
│   ├── ratelimit.py
│   ├── requirements.txt
│   └── tests/
├── web/
│   ├── index.html
│   ├── styles.css
│   └── js/
├── .streamlit/
└── README.md
```

- `streamlit_app.py`: Streamlit application entry point.
- `dashboard_pro.py`: Interactive dashboard components.
- `backend/main.py`: FastAPI application and API routes.
- `backend/analysis.py`: Data analysis operations.
- `backend/charts.py`: Chart generation.
- `backend/ml.py`: Machine learning workflows.
- `backend/parsing.py`: Data import and parsing.
- `backend/tests/`: Automated backend tests.
- `web/`: HTML, CSS, and JavaScript interface.
- `backend/requirements.txt`: Python dependencies.

## Getting Started

### Prerequisites

- Python 3.11 or 3.12 is recommended for the supplied dependency versions.
- Git, if cloning the repository.
- A modern web browser.
- Internet access during the initial dependency installation.

### 1. Clone the repository

Replace `YOUR_USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR_USERNAME/data-analyzer.git
cd data-analyzer
```

Alternatively, download the repository as a ZIP file from GitHub and extract it.

### 2. Create a virtual environment

**Windows:**

```powershell
python -m venv backend/venv
backend\venv\Scripts\activate
```

**macOS or Linux:**

```bash
python3 -m venv backend/venv
source backend/venv/bin/activate
```

If your system uses a Python launcher, select an installed compatible version explicitly.

### 3. Install dependencies

Run this command from the project root:

```bash
python -m pip install -r backend/requirements.txt
```

## Running the Application

Choose either interface.

### Option A: Streamlit

From the project root, activate the virtual environment if necessary, then run:

```bash
streamlit run streamlit_app.py
```

Open the local URL printed in the terminal, normally:

`http://localhost:8501`

Configure login credentials using the documented local secrets or environment-variable setup. Do not commit real credentials to GitHub.

### Option B: FastAPI with JavaScript frontend

Activate the virtual environment and run:

```bash
cd backend
python -m uvicorn main:app --reload --port 8010
```

Open:

`http://localhost:8010`

The FastAPI application serves the web interface and API from the same address.

Run a single worker when using the default in-memory dataset store. Restarting the backend may clear stored datasets.

## Running Tests

From the project root, activate the virtual environment and execute:

```bash
python -m pip install -r backend/requirements-dev.txt
cd backend
python -m pytest -q
```

Review the test results before reporting that the test suite passes.

## Security and Limitations

- Do not commit passwords, API keys, private environment files, or production credentials.
- Web data retrieval should be used only for accessible sources and in accordance with the target website's terms and access rules.
- Uploaded datasets and analysis results may be subject to application resource limits.
- The default dataset store is in memory and is not a persistent database.
- This project is intended for local development unless additional production deployment, authentication, and security measures are configured.

## Future Improvements

- Add more visualization and data-cleaning options.
- Improve validation and error messages for uploaded datasets.
- Add export options for reports and processed data.
- Introduce persistent storage for saved workspaces.
- Add deployment instructions and a hosted demonstration.
- Expand automated testing and continuous integration.

## Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes and test them.
4. Commit your changes with a descriptive message.
5. Open a pull request describing the improvement.

## License

No license has been specified yet. Before making the project available for reuse, add a suitable license file and confirm that the dependencies and any included assets permit your intended distribution.

## Author

**ANANYA**

- GitHub: https://github.com/Ananya11-yup

If you find this project useful, consider giving the repository a star.
