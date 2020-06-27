# Nginx Reverse Proxy

Only one service on port 80 is exposed, however there's another service running on port 8080. http://127.0.0.1/app1/ is mapped to proxy traffic to http://127.0.0.1:8080 which cannot be accessed directly by that port. http://127.0.0.1 traffic will go normaly to port 80.

## Instructions

* Run ``docker run --name some-nginx -p 80:80 -v ${PWD}/public:/usr/share/nginx/html:ro  -v ${PWD}/public2:/usr/share/nginx/html2:ro -v ${PWD}/nginx.conf:/etc/nginx/nginx.conf -d nginx``
* Navigate to ``http://127.0.0.1/app1/`` it will proxy to a web server running on 127.0.0.1:8080

### Notes

* If on Windows use PowerShell.