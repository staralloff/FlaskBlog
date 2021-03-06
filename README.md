# Intrduction

这是一个基于 [flask](https://github.com/pallets/flask)写的一个轻型博客框架。参考自:dog:[Flask Web开发 基于Python的Web应用开发实战](http://www.ituring.com.cn/book/1449)

## Dependencies

Python 2.7 least
虚拟环境安装：

```sh
$ sudo apt-get install python-virtualenv
```

所需类库依赖及版本都在requirements.txt中

## Install

在命令行中执行下述命令：

```sh
$ git clone https://github.com/staralloff/FlaskBlog.git
```

## Run

```sh
$ virtualenv venv
$ source venv/bin/activate
(venv) $ python manage.py runserver
```

Linux下配置MAIL_USERNAME和MAIL_PASSWORD

```sh
(venv) $ export MAIL_USERNAME=xxx@example.com
(venv) $ export MAIL_PASSWORD=xxxxxxxx
```

数据库的更新和数据库迁移

```sh
(venv) $ python manage.py db init
(venv) $ python manage.py db migrate -m "xxx"
(venv) $ python manage.py db upgrade
```

生成100条Post和User记录，并让用户自己关注自己

```sh
(venv) $ python manage.py shell

>>> User.generate_fake(100)
>>> Post.generate_fake(100)
>>> User.add_self_follows()
```
