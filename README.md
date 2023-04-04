# FSSen（functional , single, sentence）
Just finish your idea with single sentence!  
## concept
if done by single line, lazy to write more.
if finished by single procedure, stop next.
Maybe  it's why I prefer docker

## FIRST
> There's no doubt that job of repetitive and without improvement leads to detestation.
So, I think it nice single step for specific function, copy->paste->enter->finish.

2. change /apt/sources.list for debian-buster 
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
3. kill background task
```
jobs -l |awk '{print $2}' |xargs -n1 kill
```
4. web server concurrency test
```
ab -c 1000 -n 10000 http://ip:port/
```
5. use uwsgi to boot flask app
```
uwsgi   --http 0.0.0.0:80  --callable app --wsgi-file flask_app.py --http-keepalive --master
```
6. kill process via by its name
```
ps | grep uwsgi|awk '{print $1}'|xargs kill -9
```
