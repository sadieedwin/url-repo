# Progress Journal
- **Deployed an Ubuntu EC2 instance**
  - (opened port 5000 for Flask access)

- **Installed required packages**
```
# Ubuntu
sudo apt update -y
sudo apt install python3-pip python3-venv git -y
```

- **Set up project folder and environment**
```
mkdir url_repository
cd url_repository
```

- **Create virtual environment**
```
python3 -m venv venv
source venv/bin/activate
```

- **Install Flask and SQLAlchemy**
```
pip install flask flask_sqlalchemy
```

- **Deployed initial app files:**
  - app.py
  - models.py
  - templates/home.html
  - templates/base.html

- **Initialized database**
```
python
>>> from app import db, app
>>> with app.app_context():
...     db.create_all()

```
- **Ran the app**
```
flask run --host=0.0.0.0 --port=5000
```
- **Accessed at:**
```
http://<your-ec2-public-ip>:5000
```

- **Installed tmux for persistent server sessions**
```
sudo apt install tmux -y
```

- **Added new features:**
  - Create new link
  - Edit existing link
  - Delete link
  - Search feature
  - Filtering via tags
  - Pagination
  - Home button
