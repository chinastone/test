###  安装composer

```
wget https://mirrors.aliyun.com/composer/composer.phar    
chmod +x ./composer.phar   
mv composer.phar /usr/local/bin/composer   
composer -V
```

> 更新源 `composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/`



###  自动加载

>  注册autoloader

>  注册一个 [PSR-4](http://www.php-fig.org/psr/psr-4/) autoloader 到 `Acme` 命名空间。 `src` 会在你项目的根目录，与 `vendor` 文件夹同级。 运行 `install` 重新生成 `autoload.php`

```
{
    "autoload": {
        "psr-4": {"Acme\\": "src/"}
    }
}
```

> 代码注册

```php
$loader = require 'vendor/autoload.php';
$loader->add('Acme\\Test\\', __DIR__);
```





###  安装单个文件

```
php composer.phar update monolog/monolog
```



###  Require

```
{
    "require": {
        "monolog/monolog": "1.0.*"
    }
}
```

`>=1.0` `>=1.0,<2.0` `>=1.0,<1.1|>=1.2`

  `~1.2`相当于`>=1.2,<2.0`

### 别名

```
{
    "extra": {
        "branch-alias": {
            "dev-master": "1.0.x-dev"
        }
    }
}
```

```
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/you/monolog"
        }
    ],
    "require": {
        "symfony/monolog-bundle": "2.0",
        "monolog/monolog": "dev-bugfix as 1.0.x-dev"
    }
}
```

