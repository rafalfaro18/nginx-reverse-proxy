# Nginx Reverse Proxy

## Instructions

* Run ``docker run --name some-nginx -p 80:80 -p 8080:8080 -v ${PWD}/public:/usr/share/nginx/html:ro  -v ${PWD}/public2:/usr/share/nginx/html2:ro -v ${PWD}/nginx.conf:/etc/nginx/nginx.conf -d nginx``
* Navigate to ``http://127.0.0.1/app1/`` it will proxy to a web server running on 127.0.0.1:8080