---
title: Windows10子系统Ubuntu体验
date: 2018-06-21 10:03:20
tags: [linux,工具]
---
Windows10更新到1709（或者更早）版本后，Windows10系统自带了一个linux子系统模块，如果你想换个环境写代码，体验体验Winodws10的子系统，就可以接着往下看
{% blockquote %}
前提(必须)
1.Windows10版本在1709及以上即可
2.开发环境基于node自带npm包管理及使用Git管理代码
{% endblockquote %}
接下来教大家怎么去把玩这个系统👍
{% blockquote %}
1.先进入“控制面板”=>“程序”=>“启用或关闭Windows功能”=>找到“适用于Linux的Windows子系统”=>选中（前面打勾）=>确定然后重启电脑。
2.重启完毕后打开Windows10自带的应用商店，搜索“ubuntu”，找到下载。等下载完毕后打开，窗口会提示installing(正在安装)，等待几分钟。然后会提示输入用户名和密码，输入你喜欢的用户名和密码即可。
{% endblockquote %}
你已经安装完子系统，接下来去配置它，让它能够满足日常开发需求并且与Windows完美协作。
{% blockquote %}
1.安装node.js 按照下面依次执行 (参照https://nodejs.org/en/download/package-manager/)
{% codeblock%}
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
{% endcodeblock %}
2.安装git 按照下面执行(参照https://git-scm.com/download/linux)
{% codeblock%}
apt-get install git
{% endcodeblock %}
3.（非必须）当然，如果你要玩个人网站(hexo博客等）需要安装hexo(参照https://hexo.io/zh-cn/docs/index.html)
{% codeblock%}
npm install -g hexo-cli
{% endcodeblock %}
{% endblockquote %}
到这一步，你已经具备了开发环境所必要的工具和包，并且可以通过git拉取代码进行开发了，至于子系统的图形界面，你可以把Windows10作为子系统图形界面进行操作
{% blockquote %}
1.通过下面命令进入Windows目录
{% codeblock%}
cd /mnt
{% endcodeblock %}
2.拉取下来的项目可以随便放在你喜欢的磁盘（C、D、E、F...），通过Windows下的编程工具进行开发(like: Sublime_Text3等)
{% endblockquote %}
The End😀