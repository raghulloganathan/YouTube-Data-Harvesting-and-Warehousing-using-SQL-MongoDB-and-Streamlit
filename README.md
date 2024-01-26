# YouTube-Data-Harvesting-and-Warehousing-using-SQL-MongoDB-and-Streamlit

# YouTube Data Harvesting


#Introduction

YouTube Data Harvesting and Warehousing is a project that aims to allow users to access and analyze data from multiple YouTube channels. The project utilizes SQL, MongoDB, and Streamlit to create a user-friendly application that allows users to retrieve, store, and query YouTube channel and video data.

# Overview

This project utilizes the Streamlit library to interact with the YouTube API, fetching data about channels, playlists, videos, and comments. The retrieved data is then migrated to MongoDB and MySQL databases. Additionally, the script includes queries to extract insights from the MySQL database.

#The following technologies are used in this project:

Python: The programming language used for building the application and scripting tasks.
Streamlit: A Python library used for creating interactive web applications and data visualizations.
YouTube API: Google API is used to retrieve channel and video data from YouTube.
MongoDB: A NoSQL database used as a data lake for storing retrieved YouTube data.
SQL (MySQL): A relational database used as a data warehouse for storing migrated YouTube data.
SQLAlchemy: A Python library used for SQL database connectivity and interaction.
Pandas: A data manipulation library used for data processing and analysis.

# Features

- Fetches channel details, playlist details, video details, and comments from YouTube API.
- Migrates data to MongoDB and MySQL databases.
- Provides visualization and querying options for YouTube data.

# Prerequisites

- Python 3.x
- Required Python packages (install using `pip install -r requirements.txt`)

# Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/YouTube-Data-Harvesting.git
    cd YouTube-Data-Harvesting
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Configure API Key:

    - Replace `'YOUR_YOUTUBE_API_KEY'` with your actual YouTube API key in the script (`script.py`).

4. Run the application:

    ```bash
    streamlit run script.py
    ```

# Data Migration

# MongoDB

- Data is migrated to MongoDB in the `channel_details` collection of the `youtube_data` database.

# MySQL

- MySQL database is used with the following tables:
    - `Channel_details`
    - `Playlist_details`
    - `Video_details`
    - `Comment_details`

# Queries

1. **Query 1: What are the names of all the videos and their corresponding channels?**

    ```sql
    SELECT c.channel_name, v.video_name
    FROM channel_details AS c
    JOIN video_details AS v ON c.playlist_id = v.playlist_ids;
    ```

2. ...

   (Include other queries as per your application's needs.)

# Contributing

Feel free to contribute by opening issues or submitting pull requests.

##Once the project is setup and running, users can access the Streamlit application through a web browser. The application will provide a user interface where users can perform the following actions:

Enter a YouTube channel ID to retrieve data for that channel.
Store the retrieved data in the MongoDB data lake.
Collect and store data for multiple YouTube channels in the data lake.
Select a channel and migrate its data from the data lake to the SQL data warehouse.
Search and retrieve data from the SQL database using various search options.
Perform data analysis and visualization using the provided features.
Features

# License

This project is licensed under the [MIT License](LICENSE).

---

 # References

Streamlit Documentation: https://docs.streamlit.io/
YouTube API Documentation: https://developers.google.com/youtube
MongoDB Documentation: https://docs.mongodb.com/
SQLAlchemy Documentation: https://docs.sqlalchemy.org/
Python Documentation: https://docs.python.org/
Matplotlib Documentation: https://matplotlib.org/

**Made with ❤️ by Raghul L**

