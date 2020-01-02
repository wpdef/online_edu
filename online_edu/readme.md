###环境配置
安装django最新版
`pip install django`

安装mysqldb
`pip install mysqlclient`

####settings文件配置
```python

#模板设置
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [os.path.join(BASE_DIR,"templates")],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

#数据库配置
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'wechat',
        'USER': 'wechat',
        'PASSWORD': 'wOWlbhy8',
        'HOST': '49.235.*.*',
        'PORT': '3306',
    }
}

#语言和时区设置
LANGUAGE_CODE = 'zh-Hans'

TIME_ZONE = 'UTC'

USE_I18N = True

#静态文件
STATIC_URL = '/static/'
STATICFILES_DIR = [
os.path.join(BASE_DIR,'static'),
]
STATIC_ROOT = '/www/wwwroot/wechat/static/'

```
