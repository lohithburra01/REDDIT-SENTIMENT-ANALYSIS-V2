# Reddit Sentiment Analysis with DeepSeek LLM (Version 2)

## Overview
This project is an upgraded version of a Reddit sentiment analysis tool that now leverages the power of **Large Language Models (LLMs)** for more intelligent and customizable data extraction and sentiment analysis. Unlike the previous version, which used **PRAW API** for scraping and **VADER** for sentiment analysis, this version utilizes **DeepSeek's LLM** to extract and analyze Reddit data with greater accuracy, flexibility, and cost-efficiency.

With this tool, you can:
- **Scrape Reddit data** based on natural language instructions.
- **Analyze sentiment** using a state-of-the-art LLM for more nuanced and context-aware results.
- **Customize extraction and analysis** to fit your specific needs (e.g., focus on specific stocks like Apple or Tesla).
- **Run locally** with a locally installed DeepSeek model for completely free usage.

---

## Key Features
- **Intelligent Data Extraction**: Use natural language instructions to scrape Reddit data. For example:
  - "Extract all posts and comments related to Apple stock (AAPL)."
  - "Find discussions about Tesla (TSLA) from the last week."
- **Advanced Sentiment Analysis**: Leverage DeepSeek's LLM for sentiment analysis, which understands context and nuances better than traditional methods like VADER.
- **Customizable and Scalable**: Easily adapt the tool to analyze different topics, subreddits, or timeframes.
- **Cost-Effective**: By using DeepSeek's LLM, you can achieve high-quality results at a lower cost compared to traditional APIs.
- **Local Installation**: If DeepSeek is installed locally, you can run the entire pipeline for **free**.

---

## How It Works
1. **Scraping**: The tool uses **Crawl4AI** to scrape Reddit data based on your instructions. It can handle dynamic content and extract structured data.
2. **Sentiment Analysis**: The scraped data is analyzed using **DeepSeek's LLM**, which classifies each post/comment as **bullish**, **bearish**, or **neutral**.
3. **Results**: The tool calculates the percentage of each sentiment and saves the results in a JSON file for further analysis or visualization.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/reddit-sentiment-analysis-llm.git
   cd reddit-sentiment-analysis-llm
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your DeepSeek API key:
   - If using the DeepSeek API, add your API key to an environment variable:
     ```bash
     export DEEPSEEK_API="your_api_key_here"
     ```
   - If running DeepSeek locally, follow the installation instructions for the local model.

---

## Usage
1. **Scrape Reddit Data**:
   - Update the `URL_TO_SCRAPE` and `INSTRUCTION_TO_LLM` variables in the script to specify the Reddit URL and extraction instructions.
   - Run the scraping script:
     ```bash
     python scrape_reddit.py
     ```

2. **Analyze Sentiment**:
   - Run the sentiment analysis script:
     ```bash
     python analyze_sentiment.py
     ```

3. **View Results**:
   - The sentiment analysis results will be saved in `sentiment_results.json`.

---

## Example Output
The tool generates a JSON file with the sentiment analysis results:
```json
{
  "total_posts": 100,
  "sentiment_percentages": {
    "bullish": 45.0,
    "bearish": 30.0,
    "neutral": 25.0
  },
  "sentiment_counts": {
    "bullish": 45,
    "bearish": 30,
    "neutral": 25
  }
}
```

---

## Why This Version?
- **Better Accuracy**: LLMs like DeepSeek provide more accurate sentiment analysis by understanding context and nuances.
- **Easier Customization**: Natural language instructions make it easy to scrape and analyze specific data.
- **Cost-Effective**: Using DeepSeek's LLM is cheaper than traditional APIs, and running it locally is completely free.
- **Future-Proof**: Leveraging LLMs ensures that the tool remains relevant as AI technology advances.

---

## Future Improvements
- Add support for **real-time sentiment analysis**.
- Integrate with **visualization tools** (e.g., Matplotlib, Tableau) for better data representation.
- Expand to other platforms (e.g., Twitter, news websites).

---

## Contributing
Contributions are welcome! If you have any ideas or improvements, feel free to open an issue or submit a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- **DeepSeek** for providing the LLM used in this project.
- **Crawl4AI** for making web scraping easier and more customizable.
