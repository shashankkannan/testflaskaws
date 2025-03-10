# testflaskaws
USERDATA

sudo apt-get update -y
sudo apt-get install -y python3-pip python3-dev git python3-flask python3-mysql.connector python3-gunicorn python3-flask-cors python3-flask-sqlalchemy

cd /home/ubuntu
sudo git clone https://github.com/shashankkannan/testflaskaws.git flask-app
cd flask-app

sudo pip3 install -r requirements.txt

nohup python3 app.py > /dev/null 2>&1 &
