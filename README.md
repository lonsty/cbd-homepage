# 青岛中央商务区宣传页

此web项目基于Python3 flask框架，前端主要使用了bootstrap4框架和jQuery工具，该项目借鉴了[flack](https://github.com/miguelgrinberg/flack)。

# 1. 历史版本

##### version 1.0 (May 5 2019)

- 完成用于宣传CBD的flask web应用。

- 手机端，电脑端均可以访问宣传页，但以适配手机端为主。

# 2. 使用说明

1. 克隆远程仓库到本地

```bash
git clone https://github.com/lonsty/CBDHomepage.git
```

2. 进入项目文件夹

```bash
cd CBDHomepage
```
## 方式1：通过python3直接启动


3. 安装程序运行所需依赖包

```bash
pip3 install -r requirements.txt
```

4. 运行

```bash
export FLASK_APP=flasky && flask run -h 0.0.0.0 -p 80
```


## 方式2：docker镜像启动

3. 打包docker镜像

```bash
docker build -t cbdhome -f Dockerfile/Dockerfile .
```

4. 启动打包好的镜像

```bash
docker run --name CBDHomepage -d -p 80:80 cbdhome
```

任何一种方式运行成功后，通过浏览器打开`http://<本机IP>`即可看到项目首页。

# 3. 目录结构

```
CBDHomepage  # 项目名称
├── config.py  # 项目配置文件
├── Dockerfile
│   └── Dockerfile  # 打包docker镜像
├── flasky  # 项目源码
│   ├── api  # API拓展功能
│   │   └── __init__.py
│   ├── main.py  # 主函数，主页路由定义在此
│   ├── __init__.py
│   ├── static  # 静态资源文件夹
│   │   ├── assets  # 第三方静态资源
│   │   │   ├── animate.css
│   │   │   │   └── animate.min.css
│   │   │   ├── bootstrap
│   │   │   │   ├── css
│   │   │   │   └── js
│   │   │   ├── bootstrap-material-design-font
│   │   │   │   └── css
│   │   │   ├── dropdown
│   │   │   │   ├── css
│   │   │   │   └── js
│   │   │   ├── images
│   │   │   │   ├── logo.png
│   │   │   │   ├── mbr-2.jpg
│   │   │   │   ├── mbr-4.jpg
│   │   │   │   ├── mbr-8.jpg
│   │   │   │   └── mbr.jpg
│   │   │   ├── jarallax
│   │   │   │   └── jarallax.js
│   │   │   ├── mobirise
│   │   │   │   └── css
│   │   │   ├── smooth-scroll
│   │   │   │   ├── smooth-scroll-16.0.3.js
│   │   │   │   └── smooth-scroll.js
│   │   │   ├── tether
│   │   │   │   ├── tether.min.css
│   │   │   │   └── tether.min.js
│   │   │   ├── theme
│   │   │   │   ├── css
│   │   │   │   └── js
│   │   │   ├── touch-swipe
│   │   │   │   └── jquery.touch-swipe.min.js
│   │   │   ├── viewport-checker
│   │   │   │   └── jquery.viewportchecker.js
│   │   │   └── web
│   │   │       └── assets
│   │   ├── bootstrap-4.3.1  # bootstrap4框架
│   │   │   ├── css
│   │   │   │   ├── bootstrap.css
│   │   │   │   ├── bootstrap.css.map
│   │   │   │   ├── bootstrap-grid.css
│   │   │   │   ├── bootstrap-grid.css.map
│   │   │   │   ├── bootstrap-grid.min.css
│   │   │   │   ├── bootstrap-grid.min.css.map
│   │   │   │   ├── bootstrap.min.css
│   │   │   │   ├── bootstrap.min.css.map
│   │   │   │   ├── bootstrap-reboot.css
│   │   │   │   ├── bootstrap-reboot.css.map
│   │   │   │   ├── bootstrap-reboot.min.css
│   │   │   │   └── bootstrap-reboot.min.css.map
│   │   │   └── js
│   │   │       ├── bootstrap.bundle.js
│   │   │       ├── bootstrap.bundle.js.map
│   │   │       ├── bootstrap.bundle.min.js
│   │   │       ├── bootstrap.bundle.min.js.map
│   │   │       ├── bootstrap.js
│   │   │       ├── bootstrap.js.map
│   │   │       ├── bootstrap.min.js
│   │   │       └── bootstrap.min.js.map
│   │   ├── css  # CSS文件
│   │   │   └── index.css  # 主页CSS配置
│   │   ├── img  # 静态图片
│   │   │   ├── 4To3  # 裁剪后的4:3图片
│   │   │   │   ├── 540x405
│   │   │   │   ├── GJHYDS1.jpg
│   │   │   │   ├── GJHYDS2.jpg
│   │   │   │   ├── LSJSDS1.jpg
│   │   │   │   ├── LSJSDS2.jpg
│   │   │   │   ├── QDRMTDS1.jpg
│   │   │   │   ├── QDRMTDS2.jpg
│   │   │   │   ├── SWKJDS1-b.jpg
│   │   │   │   ├── SWKJDS1.jpg
│   │   │   │   ├── SWKJDS2.jpg
│   │   │   │   ├── ZYCTDS1.jpg
│   │   │   │   └── ZYCTDS2.jpg
│   │   │   ├── logo.png
│   │   │   ├── QD.jpg
│   │   │   ├── 中央商务区.jpg
│   │   │   ├── 卓越创投大厦1.jpg
│   │   │   ├── 卓越创投大厦2.jpg
│   │   │   ├── 国际航运大厦1.jpg
│   │   │   ├── 国际航运大厦1_pruned.jpg
│   │   │   ├── 国际航运大厦2.jpg
│   │   │   ├── 国际航运大厦2_pruned.jpg
│   │   │   ├── 生物科技大厦1-b.jpg
│   │   │   ├── 生物科技大厦1.jpg
│   │   │   ├── 生物科技大厦2.jpg
│   │   │   ├── 绿色建设大厦1.jpg
│   │   │   ├── 绿色建设大厦2.jpg
│   │   │   ├── 绿色建设大厦2_pruned.jpg
│   │   │   ├── 青岛融媒体大厦1.jpg
│   │   │   ├── 青岛融媒体大厦2.jpg
│   │   │   └── 青岛融媒体大厦2_pruned.jpg
│   │   ├── js  # JavaScript文件
│   │   │   ├── jquery-3.4.0.js
│   │   │   └── jquery-3.4.0.min.js
│   │   └── mobiriseicons  # 第三方图标
│   │       ├── 16 px
│   │       │   ├── mobirise
│   │       │   └── svg
│   │       ├── 24 px
│   │       │   ├── mobirise
│   │       │   └── svg
│   │       ├── 30 px
│   │       │   ├── mobirise
│   │       │   └── svg
│   │       └── readme.html
│   └── templates  # 页面模板
│       └── index.html  # 主页
├── LICENSE  # 项目许可证
├── manage.py  # 入口启动程序
├── README.md  # 说明文件
└── requirements.txt  # 项目第三方依赖包
```