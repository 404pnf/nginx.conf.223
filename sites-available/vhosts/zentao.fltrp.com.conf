
## HTTP server.
server {
    listen 80;
    server_name zt.fltrp.com;
    error_log   logs/error.log;
    if ($request_method !~ ^(GET|HEAD|POST)$ ) {
        return 444;
    }
    root  /var/www/zentaopms/www;
    index index.php index.html;
    autoindex on;
    location = / {
         #rewrite ^ /www/;
    }
    location / {
        proxy_pass http://apache;
    }
} # HTTP server
