# TextAnalysis & Sentiment Analysis Web App

A powerful Django-based web application designed to perform sentiment analysis on public opinion from various social media platforms and news sources. The application fetches comments, translates them to English, and utilizes advanced NLP models to classify sentiment as Positive, Negative, or Neutral.

## Key Features

- **Multi-Platform Data Fetching**:
  - **YouTube**: Uses YouTube Data API to fetch video comments.
  - **Reddit**: Uses PRAW (Python Reddit API Wrapper) to fetch discussion threads.
  - **Twitter (X)**: Implements Selenium-based automation to scrape latest tweets/comments.
  - **News Portals**: Scrapes articles and summaries from platforms like Ekantipur.
- **File Parsing**: Support for uploading CSV files containing raw text/comments for bulk analysis.
- **Multilingual Support**: Integrates `googletrans` to automatically translate non-English content before analysis.
- **Advanced NLP Engine**:
  - Powered by Hugging Face `transformers`.
  - Uses the `distilbert-base-uncased-finetuned-sst-2-english` model for high-accuracy sentiment classification.
- **Interactive Visualizations**: Generates dynamic charts (likely using Chart.js) to visualize sentiment distribution.

## Tech Stack

- **Backend**: Django, Python 3.x
- **ML/NLP**: Hugging Face Transformers, TensorFlow/Keras, NLTK
- **Data Handling**: Pandas, NumPy
- **Web Scraping & Automation**: Selenium WebDriver, Beautiful Soup
- **APIs**: YouTube Data API v3, PRAW (Reddit)
- **Frontend**: HTML5, CSS3, JavaScript (Chart.js)

## Setup & Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/umesh0518/TextAnalysis.git
   cd TextAnalysis-main
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Environment Setup**:
   - Ensure you have Chrome installed (for Selenium).
   - Configure API Keys (YouTube API, Reddit Client ID/Secret) in `webApp/views.py` or `.env`.

4. **Run the Server**:
   ```bash
   python manage.py runserver
   ```

5. **Access the App**:
   Open a browser and navigate to `http://127.0.0.1:8000`.

## Directory Structure

- `webApp/`: Core application logic (Views, Models, Forms).
- `textAnalyis/`: Project configuration and settings.
- `templates/`: HTML templates for the UI.
- `static/`: Static assets (CSS, JS, Images).
