# Media SubDomain

I'm using Wasabi as the backend, but I serve all content via a https://mediacdn.aus.social/ URL.

This will allow me to quickly switch from Wasabi to BunnyS3 once they support it, by just updating the $s3\_backend path.

## Option 1: Forwarding only

This is my config for aus.social. It forwards all requests for media to the Wasabi bucket.\
\
Example: [https://mediacdn.aus.social/accounts/avatars/000/000/001/original/30ea1ea3b78c6690.jpg](https://mediacdn.aus.social/accounts/avatars/000/000/001/original/30ea1ea3b78c6690.jpg) -> [https://s3.ap-southeast-2.wasabisys.com/aussocial/accounts/avatars/000/000/001/original/30ea1ea3b78c6690.jpg](https://s3.ap-southeast-2.wasabisys.com/aussocial/accounts/avatars/000/000/001/original/30ea1ea3b78c6690.jpg)

```
server {
  listen 443 ssl http2;
  listen [::]:443 ssl http2;
  server_name mediacdn.aus.social;
  root /var/www/html;

  keepalive_timeout 30;

  set $s3_backend 'https://s3.ap-southeast-2.wasabisys.com/aussocial';
  location / { return 302 $s3_backend$request_uri; }
  
  ssl_certificate /etc/letsencrypt/live/mediacdn.aus.social/fullchain.pem; # managed by Certbot
  ssl_certificate_key /etc/letsencrypt/live/mediacdn.aus.social/privkey.pem; # managed by Certbot
}

```

## Option 2: Local Caching

Mastodon has official documentation to use nginx as a local cache by proxying object storage through nginx. \
\
This helps if the s3 backend such as Wasabi ever goes down, but puts extra load on the nginx server and required additional local storage.

[https://docs.joinmastodon.org/admin/optional/object-storage-proxy/](https://docs.joinmastodon.org/admin/optional/object-storage-proxy/)\


