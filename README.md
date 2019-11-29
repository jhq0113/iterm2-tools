mac下使用lrzsz
=============

* [1.下载lrzsz](#下载lrzsz)
* [2.下载iterm2,傻瓜式安装即可](#下载iterm2,傻瓜式安装即可)
* [3.下载iterm2-tools](#下载iterm2-tools)
* [4.配置iterm2](#配置iterm2)

下载lrzsz
========

```bash
brew install lrzsz
```

* [回到目录](#mac下使用lrzsz)

下载iterm2,傻瓜式安装即可
======================

[下载地址](https://iterm2.com/)


* [回到目录](#mac下使用lrzsz)

下载iterm2-tools
===============

[下载地址](https://github.com/jhq0113/iterm2-tools)

* 将`iterm2-recv-zmodem.sh`与`iterm2-send-zmodem.sh`文件放到`/usr/local/bin`目录,并添加执行权限，命令如下：

```bash
sudo cp iterm2-recv-zmodem.sh /usr/local/bin
sudo cp iterm2-send-zmodem.sh /usr/local/bin
sudo chmod +x /usr/local/bin/iterm2-*
```

* [回到目录](#mac下使用lrzsz)

配置iterm2
=========

* 打开iterm2，然后快捷键`command+,`，按下图点击`edit`
![image](https://github.com/jhq0113/iterm2-tools/raw/master/iterm2.png?raw=true)

* 按照下图配置：
![image](https://github.com/jhq0113/iterm2-tools/raw/master/rzsz.png?raw=true)

* 配置内容如下：
```bash
Regular expression: rz waiting to receive.\*\*B0100
Action: Run Silent Coprocess
Parameters: /usr/local/bin/iterm2-send-zmodem.sh

Regular expression: \*\*B00000000000000
Action: Run Silent Coprocess
Parameters: /usr/local/bin/iterm2-recv-zmodem.sh
```

配置完即可使用。

* [回到目录](#mac下使用lrzsz)

