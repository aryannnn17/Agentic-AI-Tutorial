# Blood Report Analysis

## Concept

This folder demonstrates how to use LLMs to analyze medical blood reports. It shows a two-stage process:
1. **Data Extraction**: Extract structured test values from unstructured blood report text and classify them as HIGH, LOW, or NORMAL based on reference ranges
2. **Health Analysis**: Generate a health summary and personalized diet plan based on the extracted data

This demonstrates LLM's ability to understand medical data, extract structured information, and provide actionable recommendations.

## What Was Used

- **Google Gemini API**: Used `langchain-google-genai` with gemini-3.1-flash-lite model
- **LangChain**: Framework for LLM integration
- **Python-dotenv**: For managing API keys
- **Streamlit**: Web application framework for the interactive app (in `streamlit-app/` folder)

## How to Run

### Option 1: Jupyter Notebook

1. **Set up environment variables**:
   - Copy `.env.example` to `.env` in the project root
   - Add your Google API key:
     ```
     GOOGLE_API_KEY=your_google_api_key
     ```

2. **Open the notebook**:
   - Open `blood-analysis.ipynb` in Jupyter
   - Run cells sequentially to see the two-stage analysis process

3. **The notebook demonstrates**:
   - Loading blood report data from `blood_report.txt`
   - Extracting test values with status classification
   - Generating health summary and Gujarati Indian diet plan

### Option 2: Streamlit App

1. **Navigate to the streamlit-app folder**:
   ```bash
   cd 2-blood-report-analysis/streamlit-app
   ```

2. **Run the Streamlit app**:
   ```bash
   streamlit run app.py
   ```

3. **Use the web interface** to upload blood reports and get instant analysis

## Sample Data

The `blood_report.txt` file contains a sample blood report for a 40-year-old male patient with various test results including CBC, Lipid Panel, Metabolic Panel, and Liver Function tests.
