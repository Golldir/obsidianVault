## Nginx 
#### **/etc/nginx/sites-available/ | /etc/nginx/sites-enabled/**
```nginx
server {
    listen 80;
    server_name 192.168.1.50;

    location = /favicon.ico { access_log off; log_not_found off; }
    location /static/ {
        root /home/golldir/PycharmProjects/Argus3.1/Argus_WebServer;
    }

    location / {
        include proxy_params;
        proxy_pass http://unix:/run/gunicorn.sock;
    }
}
```

## Gunicorn
#### /etc/systemd/system/gunicorn.service
```systemd
[Unit]
Description=gunicorn daemon
Requires=gunicorn.socket
After=network.target

[Service]
User=golldir
Group=www-data
WorkingDirectory=/home/golldir/PycharmProjects/Argus3.1/Argus_WebServer
ExecStart=/home/golldir/PycharmProjects/Argus3.1/Argus_venv/bin/gunicorn \
          --access-logfile - \
          --workers 3 \
          --bind unix:/run/gunicorn.sock \
          Argus_Core.wsgi:application

[Install]
WantedBy=multi-user.target

```
#### /etc/systemd/system/gunicorn.socket
```systemd
[Unit]
Description=gunicorn socket

[Socket]
ListenStream=/run/gunicorn.sock

[Install]
WantedBy=sockets.target

```
```bash
sudo systemctl start gunicorn.socket
sudo systemctl enable gunicorn.socket

sudo systemctl status gunicorn.socket
sudo journalctl -u gunicorn.socket
```
## Redis
#### Bash
```bash
sudo apt install redis
sudo systemctl enable redis-server
redis-cli
```
setting.py
```python
REDIS_HOST = 'localhost' 
REDIS_PORT = '6379' 
BROKER_URL = 'redis://' + REDIS_HOST + ':' + REDIS_PORT + '/0' 
BROKER_TRANSPORT_OPTIONS = {'visibility_timeout': 3600} 
CELERY_RESULT_BACKEND = 'redis://' + REDIS_HOST + ':' + REDIS_PORT + '/0'
```
## Celery 
#### /etc/systemd/system/celery.service
```systemd
[Unit]
Description=Celery Service
After=network.target

[Service]
WorkingDirectory=/home/golldir/PycharmProjects/Argus3.1/Argus_WebServer
Environment="PATH=/home/golldir/PycharmProjects/Argus3.1/Argus_venv/bin"
ExecStart=/home/golldir/PycharmProjects/Argus3.1/Argus_venv/bin/celery -A  Argus_Celery.celery worker --loglevel=info

[Install]
WantedBy=default.target

```