# Personalized News Aggregator

## Overview
The Personalized News Aggregator is a Streamlit-based Python application that allows users to fetch and summarize news articles on any topic of their choice. Using the NewsAPI and Hugging Face's summarization pipeline, the app displays concise article summaries and generates a word cloud based on the fetched articles' content.

---

## Features
- **Search for News Articles:** Enter a topic or keyword to retrieve relevant news articles.
- **Article Summarization:** Automatically summarize long articles using Hugging Face's `transformers` library.
- **Word Cloud Generation:** Create a visual representation of the most common words in the fetched articles.
- **Interactive Interface:** Simple and user-friendly design using Streamlit.

---

## Requirements
To run this application, you need the following:

### Python Libraries:
- `streamlit`
- `requests`
- `transformers`
- `wordcloud`
- `matplotlib`

### API Key:
- A valid API key from [NewsAPI](https://newsapi.org/).

---

## Installation
1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd personalized-news-aggregator
   ```

2. **Install Dependencies:**
   ```bash
   pip install streamlit requests transformers wordcloud matplotlib
   ```

3. **Get NewsAPI Key:**
   - Sign up at [NewsAPI](https://newsapi.org/) to get a free API key.
   - Replace `'your_newsapi_key_here'` in the code with your actual API key.

---

## Usage
1. **Run the Application:**
   ```bash
   streamlit run personalized_news.py
   ```

2. **Enter Search Query:**
   - Enter a topic or keyword (e.g., "AI", "Technology").

3. **Adjust Article Count:**
   - Use the slider to select the number of articles to fetch (1 to 10).

4. **View Results:**
   - Article summaries will be displayed along with the source and a link to the full article.
   - A word cloud will be generated to visualize common topics.

---

## Troubleshooting
### Common Issues:
1. **Error: `401 - Your API key is invalid or incorrect.`**
   - Ensure that your NewsAPI key is valid and correctly entered in the code.
   - You can test the key with a simple request:
     ```python
     import requests

     API_KEY = 'your_actual_api_key'
     BASE_URL = 'https://newsapi.org/v2/everything'
     response = requests.get(BASE_URL, params={'q': 'AI', 'apiKey': API_KEY})
     print(response.json())
     ```

2. **No Content to Summarize:**
   - Some articles may not have enough content for summarization. These will be skipped.

---

## Credits
- **NewsAPI**: For fetching news articles.
- **Hugging Face Transformers**: For text summarization.
- **Streamlit**: For the interactive web app framework.
- **WordCloud & Matplotlib**: For generating word clouds and visualizations.

---

## License
This project is open-source and available under the MIT License.

---

## Built By
Asem 🚀

