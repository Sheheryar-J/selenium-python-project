# selenium-python-project
This project is python based web scraper that extracts information about topics and their repositories from the url"https://github.com/topics" page. Using 'requests','BeautifulSoup', and 'pandas'.The script collects topic titles, descriptions, URLs and repository details(e.g. repository name, owner,star count, and URL). The data is saved in CSV format for further analysis. 

**Features:-**
- Scrape and save github topics, including:-
       - Topic titles
       - Topic descriptions
       - Topic URLs
- Scrape repository information for each topic, including:-
       - Repository owner(username)
       - Repository name
       - Repository stars
       - Repository URL
 - Save the scraped data to CSV files
 - Automatically handle pre-existing files to avoid overwriting.

**Technologies used**
- **Python**: Programming Language
- **Libraries**-
    -'requests': For sending HTTP requests to GitHub
    - 'BeautifulSoup'(from 'bs4'): For parsing HTML content
    - 'pandas': For organizing and saving data in CSV format
    - 'os': For file and directory operations

**Prerequisites**
  1. Python 3.*.* installed.
  2. Install the required libraries:
      '''bash
     pip install requests beautifulSoup4 pandas

**Usage**
1. Clone the repository:
    '''bash
   git clone<repository_url>
   cd<repository_name>
   '''
2. Run the jupyter notebook cell:
     -click the play button on top left of each cell in vs code

3. The script performs the following:
   - Scrapes all topics from the Github Topics page
   - Saves the topics and their descriptions in 'topics.csv'.
   - Scrapes the top repositories for each topic.
   - Saves the repository data for each topic in 'data/' directory as CSV files

4. Explore the saved CSV files for insights.

##Functions
### Scraping Functions
- **`get_topic_titles(doc)`**: Extracts topic titles from the HTML document.
- **`get_topic_descs(doc)`**: Extracts topic descriptions.
- **`get_topic_urls(doc)`**: Extracts topic URLs.

### Repository Functions
- **`get_topic_page(topic_url)`**: Fetches and parses the topic page.
- **`get_repo_info(h1_tag, star_tag)`**: Extracts repository owner, name, stars, and URL.
- **`get_topic_repos(topic_doc)`**: Extracts repository information for a given topic.

### General Functions
- **`scrape_topic(topic_url, path)`**: Scrapes repositories for a single topic and saves the data to a CSV file.
- **`scrape_topics()`**: Scrapes all topics and returns a DataFrame.
- **`scrape_topics_repos()`**: Scrapes topics and their repositories and saves the data to the `data/` directory.    






