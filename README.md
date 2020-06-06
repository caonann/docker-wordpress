# docker-wordpress
run wordpress with docker compose
docker创建wordpress网站，支持https

```
docker-compose up -d
```

```
#配置https
docker-compose exec wordpress_tls /opt/letsencrypt/certbot-auto --apache -d your.domain.com --agree-tos -n -m you@your.domain.com
```

```
证书过期执行
docker-compose exec wordpress_tls /opt/letsencrypt/certbot-auto renew
加入crontab
0 0 1 * * docker-compose exec wordpress_tls /opt/letsencrypt/certbot-auto renew
```


