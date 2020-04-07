auto_install
============

自动装机系统，可以配置ILO，RAID,通过PXE启动，自动发现机器添加到装机系统中，目前执行机型，DELL,IBM,浪潮，华为 ,HP

以前工作中经常大批量服务器上线每次大概50台~100台左右，可就我一个人来安装配置。
开始的时候用得cobbler，可以完成操作系统的安装。做成一个虚拟机，直接接入交换机或者对插服务器。
刚开始觉得还可以，可后来新的服务器都没有配置raid就得手工一台一台配置比较烦。于是就在github上找到这个项目https://github.com/gaoming655/auto_install得改进，当时看了下介绍符合我的预期。
就是安装配置文档比较少，在读完源码后，做了点修改后搭建起来。多年后觉得是个好项目推荐出来。
-----------------
依赖组件
*   python 1.7+
*   Django 1.7
*   request
*   python-memcached
*   mysql-python

------------------
目录结构

        auto_install/
        ├── auto_install
        │   ├── __init__.py
        │   ├── settings.py
        │   ├── urls.py
        │   └── wsgi.py
        ├── conf_file
        ├── manage.py
        ├── pxe
        │   ├── admin.py
        │   ├── forms.py
        │   ├── __init__.py
        │   ├── models.py
        │   ├── tests.py
        │   └── views.py
        ├── static
        │   ├── boot
        │   │   ├── css
        │   │   │   ├── bootstrap.css
        │   │   │   ├── bootstrap.min.css
        │   │   │   ├── bootstrap-theme.css
        │   │   │   ├── bootstrap-theme.min.css
        │   │   │   ├── scojs.css
        │   │   │   └── sco.message.css
        │   │   ├── fonts
        │   │   └── js
        │   │       ├── ajax.js
        │   │       ├── bootstrap.js
        │   │       ├── bootstrap.min.js
        │   │       ├── jquery.js
        │   │       ├── npm.js
        │   │       ├── sco.confirm.js
        │   │       ├── sco.modal.js
        │   │       └── sco.valid.js
        │   └── images
        ├── templates
        │   ├── base.html
        │   ├── edit.html
        │   ├── exe.html
        │   ├── find.html
        │   ├── his.html
        │   ├── info.html
        │   ├── install.html
        │   ├── ks
        │   │   ├── conf.cfg
        │   │   └── webserver.cfg
        │   └── login.html
        └── tools
            ├── auto_install.sh
            ├── index.py
            └── post.sh
![截图](https://raw.githubusercontent.com/gaoming655/auto_install/master/static/boot/images/jt_login.jpg) 

![截图](https://raw.githubusercontent.com/gaoming655/auto_install/master/static/boot/images/jt.jpg)  

![截图](https://raw.githubusercontent.com/gaoming655/auto_install/master/static/boot/images/info.jpg)  

![截图](https://raw.githubusercontent.com/gaoming655/auto_install/master/static/boot/images/edit.jpg) 

![截图](https://raw.githubusercontent.com/gaoming655/auto_install/master/static/boot/images/jd.jpg)

![截图](https://raw.githubusercontent.com/gaoming655/auto_install/master/static/boot/images/wancheng.jpg)
