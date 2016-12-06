## phpcs的自动检测及提交钩子hook脚本

### 参考代码,文章

* [Pre-commit hook for git with phpcs and phpcbf (auto-correct obvious violations)](https://gist.github.com/fdemiramon/0423b4308218d417fbf3)
* [hootsuite/pre-commit-php](https://github.com/hootsuite/pre-commit-php)
* [s0enke/git-hooks/phpcs-pre-commit](https://github.com/s0enke/git-hooks/tree/master/phpcs-pre-commit)
* [bupt1987/git-hooks](https://github.com/bupt1987/git-hooks)

### 特性

* 自动检测并按指定标准修订代码
* 相关设置可配置或自动检测

### 安装

1. 拷贝 phpcs_config 和 pre-commit 到项目的.git/hooks路径下
2. (可选)根据项目的相关需求修改phpcs_config中的设置

### 配置

* `PHPCS_BIN` 指定 phpcs可执行代码的完整路径
* `PHPCBF_BIN` 指定 phpcbf可执行代码的完整路径
* `PHPCS_CODING_STANDARD` 指定phpcs所使用的编码规范（默认PSR2）

#### 其他说明

* 项目内安装phpcs,phpcbf,composer.json配置文件的require-dev段 中加入:
```
    "require-dev": [
        "squizlabs/php_codesniffer": "2.0.*@dev"
    ],
```
即可使用 vendor/bin/phpcs工具
