# Movie Ranking Web App

This is a Flask-based web application that allows you to manage and rank your favorite movies. It integrates with The Movie Database (TMDb) API to fetch movie information and uses SQLite for local data storage.

## Features

* **View Ranked Movies:** See a list of your movies, automatically ranked by your custom rating.
* **Add New Movies:** Search for movies using The Movie Database (TMDb) and add them to your list.
* **Rate and Review Movies:** Assign a rating (out of 10) and write a personal review for each movie.
* **Edit Movie Details:** Update the rating and review of existing movies.
* **Delete Movies:** Remove movies from your list.

## Setup

Follow these steps to get the project up and running on your local machine.

### 1. Clone the Repository (if applicable)

If you're getting this code from a repository, clone it first:

```bash
git clone <repository_url>
cd <repository_name>
```

### 2. Install Dependencies

This project uses several Python libraries. You can install them using `pip`.

Open your terminal or PyCharm's built-in terminal (usually at the bottom left) and run the appropriate command:

**On Windows:**

```bash
python -m pip install -r requirements.txt
```

**On macOS/Linux:**

```bash
pip3 install -r requirements.txt
```

### 3. Get a TMDb API Key

This application relies on The Movie Database (TMDb) API to search for movies and fetch their details.

1.  Go to [The Movie Database (TMDb) website](https://www.themoviedb.org/).
2.  Sign up for a free account.
3.  Once logged in, navigate to your **Account Settings**.
4.  Find the **API** section and request a new API key.
5.  Copy your **API Key (v3 auth)**.

### 4. Configure Your API Key

In the `main.py` file, find the line:

```python
MOVIE_DB_API_KEY = "USE_YOUR_OWN_CODE"
```

Replace `"USE_YOUR_OWN_CODE"` with your actual TMDb API key:

```python
MOVIE_DB_API_KEY = "YOUR_ACTUAL_TMDB_API_KEY_HERE"
```

### 5. Run the Application

Once you have installed the dependencies and configured your API key, you can run the Flask application.

In your terminal or PyCharm, execute:

```bash
python main.py
```

The application will start, and you should see output similar to this:

```
* Serving Flask app 'main'
* Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
* Running on http://127.0.0.1:5000
Press CTRL+C to quit
* Restarting with stat
* Debugger is active!
* Debugger PIN: ...
```

Open your web browser and navigate to `http://127.0.0.1:5000` to start using the application.

## Project Structure

* `main.py`: The core Flask application file containing all routes, database models, and forms.
* `templates/`: Directory for HTML template files.
    * `index.html`: Displays the main list of movies.
    * `add.html`: Page to search and add new movies.
    * `select.html`: Displays search results for movie selection.
    * `edit.html`: Page to rate and review a movie.
* `requirements.txt`: Lists all Python dependencies required for the project.
* `movies.db`: The SQLite database file (will be created automatically on first run).

## Technologies Used

* **Flask:** Web framework for Python.
* **Flask-Bootstrap5:** Integrates Bootstrap 5 for responsive and modern UI.
* **Flask-SQLAlchemy:** ORM (Object Relational Mapper) for interacting with the SQLite database.
* **SQLAlchemy:** Python SQL toolkit and ORM.
* **Flask-WTF:** Simplifies form creation and validation.
* **requests:** HTTP library for making API calls to TMDb.
* **SQLite:** Lightweight, file-based database.

---
