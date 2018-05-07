## linux 开启服务

> 开启Nginx
> ```
> /usr/local/webserver/nginx/sbin/nginx
> /usr/local/webserver/nginx/sbin/nginx -s reload # 重新载入配置文件
> /usr/local/webserver/nginx/sbin/nginx -s reopen # 重启 Nginx
> /usr/local/webserver/nginx/sbin/nginx -s stop   # 停止 Nginx
> ```

> 宿主机无法访问虚拟机中的Nginx（解决办法）
> ```
> [root@localhost html]# /sbin/iptables -I INPUT -p tcp --dport 80 -j ACCEPT   (一般执行此步骤即可)
> [root@localhost html]# /etc/init.d/iptables save  
> [root@localhost html]# /etc/init.d/iptables restart
>```

> 开启Mysql
> ```
> 开启：service mysqld start 
> 停止：service mysqld stop
> 重启：service mysqld restart
> 重载配置：service mysqld reload
> ```

> 开启PhP
> ```
> /etc/init.d/php-fpm start
> ```

