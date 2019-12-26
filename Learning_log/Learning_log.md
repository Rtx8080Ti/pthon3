# 2019年12月26日
Ubuntu 19.10 & Windows 1909 & macOS 10.15.2
python 3.7.5

问题1：Ubuntu终端不识别 python 命令，提醒可以安装，提醒已安装python3，但是需要执行 python3 命令。
平台：Ubuntu 19.10 
解决办法：
Ubuntu19.10切换python3和python2
切换Python3为默认版本：
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 100
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 150
切换Python2为默认版本：
sudo update-alternatives --config python



