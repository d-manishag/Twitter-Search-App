# Twitter-Search-App
Twitter Search Application delves into the plethora of tweets. This app retrieves, stores, and searches tweets, retweets, quoted tweets and replies with the data stored and managed using MySQL &amp; MongoDB databases. A user-friendly interface is provided with many search options. LRU caching enables the faster retrieval of data. Now keep Twitter data accessible and at hand.
To keep the system running smoothly, the cache is frequently saved to disk and stale entries are eliminated.
The search program offers a variety of search possibilities, including drill-down search tools and searches by string, hashtag, and user.

This repository has the following structure:

```
├── data/
│   └── ...
├── docs/
│   ├── FinalReport.md
│   └── ...
├── presentation/
│   └── ...
└── src/
    ├── cache/
    ├── datastore/
    ├── search/
    └── ...
```
# Setup 
(Installation and steps for publishing the app)
- Python 3.6 & above
- MySQL (’mysql-connector-python’ library to interact with MySQL)
- MongoDB(The code uses the ’pymongo’ library to interact with
MongoDB)

# Database Design 
- MySQL - The user-specific data from the JSON is retrieved, i.e., the user object in tweets with key-value pairs.
User data is procured with user-id, username, user description, number of followers, and the date the
account was created.
- MongoDB - As the idea is to efficiently store the data for fast access, the data
is stored in four collections in non-relational databases. MongoDB database is designed to store tweets,
retweets, quoted tweets, and in replies. Each collection in the tweets database holds the relevant data.
While processing the data the duplicates are supervized

# Streamlit Python
Streamlit is a free and open-source framework to rapidly build and share beautiful machine learning and data science web apps. 
Provides a Streamlit web application to search through the stored data with the flexibility of using various parameters such as usernames, 
hashtags, and date ranges.

# Testing App Functionality

1. **Clone the repository:** Clone this repository to your local machine using `git clone`.

    ```bash
    git clone https://github.com/d-manishag/Twitter-Search-App.git
    ```

2. **Install Python dependencies:** Navigate to the project directory and install the required Python packages. It is advised to carry out this task in a virtual setting.



3. **Run the data insertion notebook:** Run `data_insertion_v2.ipynb` to fetch and store the Twitter data.

    ```bash
    jupyter notebook data_insertion_v2.ipynb
    ```

4. **Run the Streamlit application:** Finally, launch the Streamlit application.

    ```bash
    streamlit run search_app.py
    ```

    Open the provided local URL in your browser to interact with the application.

