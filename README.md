# how to connect to IT with an exeter account
使用exeter的账户连接学校的超算（懒得加页面了，就这么看得了）
超算远程连接指南

不会空行，后面<作为空行符


# Exeter IT超算连接使用指南

1、拥有一个exeter邮箱并完成邮箱注册相关操作





<

2、进入官网，使用exeterVPN：：：https://www.exeter.ac.uk/departments/it/howdoi/vpn/

（下载软件，第一道输入：[remote.exeter.ac.uk](http://remote.exeter.ac.uk/)，第二道输入用户名（user‘s name，不是邮箱）和账户密码，最后click，等待成功连接）

<

https://docs.isambard.ac.uk/user-documentation/guides/login/#install-windows     （超算使用的详细操作）接下来开始介绍如何在拥有一个账户的情况下使用和连接超算

<


1、of course 你需要先获得一个invitation（找你的老师或者老板要），记得给出你的Exeter邮箱

<


2、先注册一个IT账户https://youtu.be/yLt00xQQm6I     ，这个油管视频详细介绍了相关操作

<


3、成功登录之后你可以发现你的主页有你有的资源，先确保你有IT资源，要不然也是巧妇难饮无米之炊

<


4、设置**UNIX username**

<img width="1776" height="650" alt="image" src="https://github.com/user-attachments/assets/d7ea6dff-e091-47ed-9eaa-75ee77032f04" />


这个页面往下翻

<


5、打开命令行

一
ssh-keygen -t ed25519 -C "your_email@exeter.ac.uk"

ssh-add $HOME\.ssh\id_ed25519

二

ssh-keygen -t rsa -b 4096 -C "your_email@exeter.ac.uk”

ssh-add $HOME\.ssh\id_rsa

二选一

<


6、输入第一行之后出现选项全部按enter（回车）跳过（当然你可以自己设置路径和密码，回车则路径默认，无密码）

<


7、命令行继续输入：

clifton auth

按照指示操作

（建议先登出IT账户，操作时重新登录，防止bug）

成功则输出：

Successfully authenticated as YOUR_EMAIL_ADDRESS (YOUR_SHORT_NAME) and downloaded SSH certificate for projects:

- PROJECT_NAME

Certificate file written to ~/.ssh/id_ed25519-cert.pub
Certificate valid for 11 hours and 59 minutes.
You may now want to run `clifton ssh-config write` to configure your SSH config aliases.

类似文字

<


8、命令行输入：

clifton ssh-config write

得到一个链接类似：6bk.aip2.isambard

ssh使用远程连接就可以了！

<



<

