# nginx
#/etc/nginx/cond.f	#nginx配置文件路径

server {

	listen 443 ssl;		#端口80或443
	
	server_name domain name;	#域名
	
	ssl on;
	
	ssl_certificate Public key;	#公钥
	
	ssl_certificate_key Private key;	#私钥
	
	ssl_session_timeout 5m;
	
	ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
	
	ssl_ciphers ECDHE-RSA-AES128-GCM-SHA256:HIGH:!aNULL:!MD5:!RC4:!DHE;
	
	ssl_prefer_server_ciphers on;
	
	
location / {

	proxy_pass http://ip:port;	#转发地址和端口
	
	}
	
}


