# URL Repository
_A simple Flask web application for saving, organizing, and viewing useful links._

## Features
- Add new links with title, URL, description, and tags
- View a list of saved links
- Pagination for easier navigation (10 links per page)
- Simple and clean user interface
- SQLite database for storage

## Technologies Used
- Python 3.12
- Flask
- Flask-SQLAlchemy
- SQLite
- Bootstrap (for styling)

## Setup Instructions
1. Clone the Repository
2. Create and Activate a Virtual Environment
```
python3 -m venv venv
source venv/bin/activate
```
3. Install Dependencies
```
pip install -r requirements.txt
```
4. Initialize the Database
```flask shell
>>> from app import db
>>> db.create_all()
>>> exit()
```
5. Run the Application
```
flask run --host=0.0.0.0 --port=5000
```
Then open your browser and visit:
http://localhost:5000/

Project Structure
```
url_repo/
│
├── app.py              # Main application file
├── models.py           # Database models
├── templates/
│   └── home.html       # HTML template
├── static/             # (Optional) Static files like CSS, JS
├── venv/               # Virtual environment
└── README.md           # This file
```

## Future Improvements

- Edit and delete links -- DONE
- Add search and filter features (e.g., by tag) -- DONE
- Add user authentication
- Migrate to a production database (e.g., PostgreSQL)
