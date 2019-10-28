# FSSen（functional , single, sentence）
Just finish your idea with single sentence!  
## 理念
能一句代码搞定的事，我就懒得多写。
能单个步骤完成的事，我就不做第二步。
`这大概也是我喜欢docker的原因。`
## FIRST
>毫无疑问，重复而且毫无改进的事情，做多了，总会让我心生厌恶。
比如呀，新机器上 python换源， apt换源。
所以，我期待能有一步搞定特定功能的代码，纵然它不怎么优雅。复制->粘贴->回车->搞定
1. 一句话搞定python换国内源。
```
mkdir ~/.pip && cat > ~/.pip/pip.conf  <<EOF
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
EOF
```
2. 一句话debian10 换源(非官方源GPG error)，还是ubuntu吧
```
cat > /etc/apt/sources.list <<EOF
deb http://mirrors.163.com/debian/ buster main non-free contrib
deb http://mirrors.163.com/debian/ buster-updates main non-free contrib
deb http://mirrors.163.com/debian/ buster-backports main non-free contrib
deb-src http://mirrors.163.com/debian/ buster main non-free contrib
deb-src http://mirrors.163.com/debian/ buster-updates main non-free contrib
deb-src http://mirrors.163.com/debian/ buster-backports main non-free contrib
deb http://mirrors.163.com/debian-security/ buster/updates main non-free contrib
deb-src http://mirrors.163.com/debian-security/ buster/updates main non-free contrib
EOF
```
