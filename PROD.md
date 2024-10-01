1. Среда
```bash
sudo apt update
sudo apt install python3-venv python3-dev libpq-dev postgresql postgresql-contrib nginx curl
```

2. Виртуальное окружение
```bash
1. mkdir ~/myprojectdir
2. cd ~/myprojectdir
3. python3 -m venv myprojectenv
4. source myprojectenv/bin/activate
5. pip install django gunicorn psycopg2-binary
```
3. Джанго
```python
django-admin startproject myproject ~/myprojectdir
nano ~/myprojectdir/myproject/settings.py

#settings.py
x = 2
ALLOWED_HOSTS = ['your_server_domain_or_IP', 'second_domain_or_IP', ..., 'localhost']

STATIC_URL = '/static/'  
  
STATIC_ROOT = BASE_DIR / 'static'  
  
STATICFILES_DIRS = [  
    os.path.join(BASE_DIR, 'Argus_App/static1/'),  
]  

MEDIA_ROOT = BASE_DIR / 'media'  
MEDIA_URL = '/media/'
```

5. local test
```bash
~/myprojectdir/manage.py makemigrations
~/myprojectdir/manage.py migrate
~/myprojectdir/manage.py createsuperuser
~/myprojectdir/manage.py collectstatic
sudo ufw allow 8000
~/myprojectdir/manage.py runserver 0.0.0.0:8000
```

6. gunicorn test + service + socket
```bash
cd ~/myprojectdir
gunicorn --bind 0.0.0.0:8000 myproject.wsgi
deactivate

---socket---
sudo nano /etc/systemd/system/gunicorn.socket

[Unit]
Description=gunicorn socket

[Socket]
ListenStream=/run/gunicorn.sock

[Install]
WantedBy=sockets.target

---service---
sudo nano /etc/systemd/system/gunicorn.service

[Unit]
Description=gunicorn daemon
Requires=gunicorn.socket
After=network.target

[Service]
User=sammy
Group=www-data
WorkingDirectory=/home/sammy/myprojectdir
ExecStart=/home/sammy/myprojectdir/myprojectenv/bin/gunicorn \
          --access-logfile - \
          --workers 3 \
          --bind unix:/run/gunicorn.sock \
          myproject.wsgi:application

[Install]
WantedBy=multi-user.target

sudo systemctl start gunicorn.socket
sudo systemctl enable gunicorn.socket

sudo systemctl status gunicorn.socket
```

`
##13123




GUNICORN
```bash

https://www.youtube.com/watch?v=YnrgBeIRtvo

source ~/PycharmProjects/Argus3.1/Argus_venv/bin/activate

gunicorn -c conf/gunicorn_config.py Argus_Core.wsgi

sudo usermod -aG golldir www-data
```
