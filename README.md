# Gen-AI-Project-Using-Llama3.1---Cold-Mail-Generator
This is end to end LLM and gen ai project that will use Llama3.1 open source LLM, chromadb (vector store), Langchain and streamlit to build a tool called cold email generator. This tools helps Software and AI services companies send cold emails to their potential clients.

# Cold Email Generator

This Streamlit application generates cold emails by extracting job details from a webpage and matching them with relevant skills in your portfolio. The app scrapes job details from the provided URL and uses a language model to generate a tailored email for each job listing.

## Features

- **Web scraping**: Extract job details directly from a URL using the `WebBaseLoader`.
- **Cold email generation**: Automatically generates personalized cold emails based on job descriptions and your portfolio.
- **Portfolio query**: Matches extracted job skills with your portfolio of links to provide additional references in the generated email.
- **Error Handling**: Displays a user-friendly error message if any issues occur during email generation.

## How It Works

1. **Input URL**: The user provides a URL for a job posting (e.g., a job listing page on a company's website).
2. **Web Scraping**: The app uses the `WebBaseLoader` to scrape and load the webpage content.
3. **Text Cleaning**: The `clean_text` utility function processes the webpage content to remove irrelevant text.
4. **Job Extraction**: The language model (`llm`) identifies job-related details (like responsibilities, requirements, etc.).
5. **Skill Matching**: The app compares extracted job skills with the user's portfolio using `portfolio.query_links`.
6. **Email Generation**: Based on the job data and matched skills, the language model writes a cold email tailored to the job.
7. **Display Email**: The email is displayed in the app for the user to copy.

## Prerequisites

Before running the app, ensure you have the following:

- Python 3.7+
- Required Python packages:
  - `streamlit`
  - `langchain_community`
  - Other dependencies for `chains.py`, `portfolio.py`, and `utils.py` which should include the language model and custom portfolio handling.

## Installation

1. Clone this repository or download the project files.
2. Install the required dependencies by running:
   ```bash
   pip install streamlit langchain_community


## Running the App

streamlit run app/main.py

