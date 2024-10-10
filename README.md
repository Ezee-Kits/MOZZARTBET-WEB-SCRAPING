# MOZZARTBET-WEB-SCRAPING

The **MozzartBet Betting Scraper** automates the process of collecting betting data from MozzartBet's website. This script scrapes upcoming football matches and odds (home, draw, away) and saves the data to a CSV file for further analysis or usage in betting-related tasks.

## 📌 Features

- **Automated Data Collection**: Automatically fetches football match data, including match times and odds for MozzartBet.
- **Infinite Scroll Handling**: Loads more matches by handling the scroll and load more button interaction.
- **Duplicate Removal**: Ensures no duplicate match entries in the final CSV output.
- **Data Output**: Saves all relevant information (team names, odds, match time, etc.) into a CSV file.

## 🚀 How It Works

1. **Initialization**: The script launches a headless browser using Selenium, navigating to MozzartBet’s football section for the current date.
2. **Web Page Interaction**: The script clicks on the "Load More" button and scrolls down the page to load additional matches.
3. **Data Extraction**: Match information (such as time, home team, away team, odds) is extracted and organized into a structured format.
4. **CSV Output**: The extracted data is saved into a CSV file, located at the specified path.

### Key Components:

- **Web Scraping**: Uses Selenium and BeautifulSoup to interact with the website and parse the page content.
- **Data Structuring**: Organizes the scraped data into dictionaries for saving.
- **CSV File Management**: Manages the creation and updating of CSV files, as well as removing any duplicate entries.

## 🛠️ Requirements

Before running the script, ensure the following dependencies are installed:

- **Python 3.x**
- **Selenium**
- **BeautifulSoup**
- **Pandas**
- **LXML**

Install the required libraries via pip:
```bash
pip install selenium beautifulsoup4 pandas lxml
```

## 🏃 How to Run the Script

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Ezee-Kits/MozzartBet-Betting-Scraper.git
   ```

2. **Set up ChromeDriver**:  
   Download and install [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) for your version of Chrome. Ensure it is available in your system path.

3. **Run the Python Script**:
   ```bash
   python mozzartbet_scraper.py
   ```

4. **View Results**:  
   The scraped data will be saved in a CSV file located in the `saving_path_csv` directory.

## 📁 Output

The CSV file will contain the following columns:
- **TIME**: The time of the match.
- **HOME TEAM**: The name of the home team.
- **AWAY TEAM**: The name of the away team.
- **HOME ODD**: The odds for the home team to win.
- **DRAW ODD**: The odds for a draw.
- **AWAY ODD**: The odds for the away team to win.
- **BOOKMAKER**: The bookmaker's name, in this case, MozzartBet.

## 🔧 Future Enhancements

- **Error Handling**: Enhance error handling for dynamic website changes.
- **Multi-Sport Support**: Extend the scraper to handle other sports and markets MozzartBet offers.
- **Real-Time Updates**: Add features to run the script periodically and update the CSV file with new matches.

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 🤝 Contributing

Contributions are welcome! Feel free to open issues, suggest improvements, or submit pull requests.

