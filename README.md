# nginx
#/etc/nginx/cond.f
server {
	listen 443 ssl;
	server_name domain name;
	ssl on;
	ssl_certificate Public key;
  ssl_certificate_key Private key;
	ssl_session_timeout 5m;
	ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
	ssl_ciphers ECDHE-RSA-AES128-GCM-SHA256:HIGH:!aNULL:!MD5:!RC4:!DHE;
	ssl_prefer_server_ciphers on;

location / {
	proxy_pass http://ip:port;
	}
}
