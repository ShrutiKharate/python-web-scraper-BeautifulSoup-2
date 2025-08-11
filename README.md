# Dynamic Web Page Interaction - Exploring a Tech Blog
## Tech Blog Article Scraper (DEV.to)

This Python script scrapes the main feed of a tech blog (specifically DEV.to) to fetch the titles and URLs of the most recent articles. It serves as a practical example of real-world web scraping, demonstrating how to handle common challenges like changing HTML structures and basic anti-scraping measures.

## Features ✨

-   **Targeted Scraping**: Fetches the most recent articles from the specified blog URL.
-   **Customizable Article Count**: Use the `-n` flag to specify exactly how many articles you want to retrieve.
-   **Robust Extraction**: Designed to handle a real-world website's HTML structure, which is less predictable than a wiki.
-   **Smart URL Handling**: Correctly constructs full, clickable URLs by identifying and handling both relative (`/user/post`) and absolute (`https://...`) links.
-   **Polite Scraping**: Includes a `User-Agent` header in requests to mimic a real browser, increasing the chances of a successful request.

## How to Use 🚀

1.  **Clone the repository**:
    ```bash
    git clone <your-repo-url>
    cd <your-repo-directory>
    ```

2.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the script from your terminal**:
    The script requires a URL (`-u` or `--url`) and accepts an optional number of articles (`-n` or `--num-articles`).

    ```bash
    # Scrape the 5 latest articles from DEV.to (default)
    python blog_explorer.py -u "[https://dev.to](https://dev.to)"

    # Scrape the 10 latest articles
    python blog_explorer.py --url "[https://dev.to](https://dev.to)" --num-articles 10
    ```

## Dependencies 📦

-   `requests`
-   `beautifulsoup4`

## Key Concepts Demonstrated

-   **Real-World Scraping**: Targeting a live, production website whose HTML structure can and does change over time.
-   **Handling Anti-Scraping**: Using request headers (`User-Agent`) to ensure successful fetching of page content.
-   **Adaptive Selectors**: Using class-based selectors (`find_all('div', class_='...')`) which are common on modern websites.
-   **Data Cleaning**: Implementing logic to differentiate between relative and absolute URLs to ensure all extracted links are valid.
-   **Debugging and Adaptation**: The script's development involved inspecting a live site and adapting the code to its specific structure, a core skill in web scraping.
