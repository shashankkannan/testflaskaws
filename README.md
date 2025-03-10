# testflaskaws

#!/bin/bash

# Update and install dependencies
sudo apt-get update -y
sudo apt-get install -y python3-pip python3-dev git python3-flask python3-mysql.connector python3-gunicorn python3-flask-cors python3-flask-sqlalchemy

# Clone repo
cd /home/ubuntu
sudo git clone https://github.com/shashankkannan/testflaskaws.git flask-app
cd flask-app

# Install other dependencies via pip (if needed)
# Use pip3 for any Python packages that are not available via apt
sudo pip3 install -r requirements.txt

# Run Flask app in the background
nohup python3 app.py > /dev/null 2>&1 &
