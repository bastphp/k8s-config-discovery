# install

```
composer require kuke/k8s-config-discovery
```

# desc
完美融合hyperf官方的config-center,提供autoload目录下的项目启动后配置的热更新,解决php项目使用k8s的configMap作为配置中心的问题.

# useAge
```
//config_center新加配置

'k8s' => [
            'driver' => Kuke\K8sConfigDiscovery\K8sDriver::class,//驱动文件
            'interval' => 3,//扫描时间
            'base_path' => 'config/autoload/',//要热更新的文件目录
            'listener_config' => [
                'kuke_test.php',
                'kuke_test1.php',
            ]//要监听的文件
        ]
    ],

```
