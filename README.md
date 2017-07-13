# test__postcss-loader

run the command ``` npm i ``` and then ``` npm run build_dev ```

nginx config in the vagrant
```
server {
    listen 80;
    server_name www.test__postcss-loader.local;

    root /vagrant/test__postcss-loader/dist;
    index index.html index.php;

    location / {
        sendfile  off;
        try_files $uri $uri/ /index.html;
    }
gzip on;
gzip_disable "msie6";

gzip_comp_level 6;
gzip_min_length 1100;
gzip_buffers 16 8k;
gzip_proxied any;
gzip_types
    text/plain
    text/css
    text/js
    text/xml
    text/javascript
    application/javascript
    application/x-javascript
    application/json
    application/xml
    application/rss+xml
    image/svg+xml;
}
```
