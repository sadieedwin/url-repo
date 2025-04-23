# URL Repository
_A simple Flask web application for saving, organizing, and viewing useful links._

## Why this project?
_As someone in Ops, we constantly rely on links—runbooks, monitoring dashboards, internal tools, Jira tickets, Confluence pages, knowledge base articles, vendor portals, etc. Having them all in one searchable, customizable place instead of scattered across browser bookmarks is a huge productivity boost._


## Features
- Add new links with title, URL, description, and tags
- View a list of saved links
- Simple and clean user interface

## Technologies Used
- Frontend: HTML, CSS
- Backend: Python (Flask)
- Database: SQLite for now
- OS: Ubuntu (Linux) - EC2 instance

## Screenshots
![image](https://github.com/user-attachments/assets/29f50a1e-eb41-4f2c-ae5a-12b7883a0459)
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
