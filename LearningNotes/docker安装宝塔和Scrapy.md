安装宝塔

```
docker run -i -t -d --name baota -p 20:20 -p 21:21 -p 80:80 -p 443:443 -p 888:888 -p 8888:8888 --privileged=true -v /home/www:/www centos /bin/bash
```

```
docker exec -it baota /bin/bash
```

docker里 php7.4/7.3 libonig.so.5: cannot open shared

```
yum install oniguruma - y
yum install libsodium -y
```

宝塔配置laravel

```php
从软件商店中找到php，设置：
PHP 函数解禁 proc_open、symlink、putenv
PHP 扩展安装 fileinfo、opcache、imagemagick、imap、exif、intl、xsl
redis队列：1. 安装redis 2.启动redis redis-server
队列-去除禁用函数：pcntl_signal，pcntl_alarm
```

安装Scrapy

```
docker run -tid -v /var/www/spider:/var/www/spider --name spider ubuntu /bin/bash
```

-tid :后台运行

-v 表示挂载点，把本地的目录/spider映射到容器里面的/spider

--name 给容器起个名字叫spider

/bin/bash: 登陆的shell

进入容器当中：

```
docker exec -ti spider /bin/bash
```

安装Scrapy

```
apt install python3 python3-dev python3-pip libxml2-dev libxslt1-dev zlib1g-dev libffi-dev libssl-dev
```

```
pip install scrapy
```

创建项目

```
scrapy startproject novelScrapy
```

创建爬虫

```
scrapy genspider novel www.alleylone.com
```

启动爬虫

```
scrapy crawl novel(爬虫名）
```

