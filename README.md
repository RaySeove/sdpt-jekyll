
域名绑定、301转向及nginx配置
-----

新建配置文件: ``sudo nano /etc/nginx/sites-available/sdyea.org``

编辑配置文件及保存: 

    server {
        server_name sdyea.org;
        return 301 http://www.sdyea.org$request_uri;
    }
    server {
        server_name www.sdyea.org;
        index index.html;
        root /srv/sdpt-jekyll/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name huangluoting.sdyea.org;
        index index.html;
        root /srv/huangluoting.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name lizebin.sdyea.org;
        index index.html;
        root /srv/lizebin.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name yanhui.sdyea.org;
        index index.html;
        root /srv/yanhui.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name chenzhiyi.sdyea.org;
        index index.html;
        root /srv/chenzhiyi.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name yezong.sdyea.org;
        index index.html;
        root /srv/yezong.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name lili.sdyea.org;
        index index.html;
        root /srv/lili.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name wushengtang.sdyea.org;
        index index.html;
        root /srv/wushengtang.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name luoyayun.sdyea.org;
        index index.html;
        root /srv/luoyayun.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name liweiying.sdyea.org;
        index index.html;
        root /srv/liweiying.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name wumeixia.sdyea.org;
        index index.html;
        root /srv/wumeixia.sdyea.org/_site;
        error_page 404 /Error.html;
    }
    server {
        server_name chenyitong.sdyea.org;
        index index.html;
        root /srv/chenyitong.sdyea.org/_site;
        error_page 404 /Error.html;
    }

建立链接: ``sudo ln -s /etc/nginx/sites-available/sdyea.org /etc/nginx/sites-enabled/``

重启nginx: ``sudo service nginx restart``


下载及生成网站
-----

1. 下载网站源码: ``git clone git://github.com/zackwong/sdpt-jekyll.git``

2. 进入源码根目录: ``cd sdpt-jekyll``

3. 生成网站: ``jekyll build``


开发者
---------

* Zack Wong &lt;hzzzoo@126.com&gt;


