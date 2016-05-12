---
layout: post
title:  "Jekyll Install guide on github.io"
date:   2016-05-12 14:49:48 +0900
categories: jekyll update
---


## github,io blog 사용방법

github.io page 를 이용하여 blog 를 사용할 수 있다.
username.github.io 형태의 URL 로 접속이 가능하며,
간단한 블로그 포스팅이 가능하다.

md 를 static html 로 변환시켜주는 jeky2 를 이용하게 되면,
간단한 md 를 통해 블로그 포스팅이 가능하게 된다.


#### jeky2 설치 on Ubuntu 

Jeky2 는 static site generator 이며, ruby 기반의 free software 이다.
또한 github 의 cofounder 인 Tom Priston Werner 에 의해 개발되었다.

Step1. Install rvm
* ruby 라이브러리 설치를 위한 패키지 매니저 

```
# curl -sSL https://get.rvm.io | bash -s stable
에러 발생 시 아래 키발급을 수행한다.
# gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3

Creating group 'rvm'

Installing RVM to /usr/local/rvm/
Installation of RVM in /usr/local/rvm/ is almost complete:

  * First you need to add all users that will be using rvm to 'rvm' group,
    and logout - login again, anyone using rvm will be operating with `umask u=rwx,g=rwx,o=rx`.

  * To start using RVM you need to run `source /etc/profile.d/rvm.sh`
    in all your open shell windows, in rare cases you need to reopen all shell windows.

# cloudiaan,
#
#   Thank you for using RVM!
#   We sincerely hope that RVM helps to make your life easier and more enjoyable!!!
#
# ~Wayne, Michal & team.

```

Step2. 위에서 나타나는 source 뒤 명령을 수행한다. 
```
# source /etc/profile.d/rvm.sh 
```

Step3. ruby 최신버전 설치 
```
# rvm requirements
Checking requirements for ubuntu.
Installing requirements for ubuntu.
Updating system.........
Installing required packages: libreadline6-dev, libssl-dev, libyaml-dev, libsqlite3-dev, sqlite3, autoconf, libgmp-dev, libgdbm-dev, libncurses5-dev, automake, libtool, bison, libffi-dev..............
Requirements installation successful.

# rvm install 2.3.1
최신버전 확인 : https://www.ruby-lang.org/en/downloads/
```


Step4. 디폴트 버전 세팅 
```
# rvm use 2.3.1 --default
```


Step5. nodejs 설치 
```
# sudo apt-get install nodejs
```


Step6. Jeky2 설치 
```
# gem install jekyll
# jekyll -v
root@stacka:~# jekyll -v
jekyll 3.1.3

```



Step7. Blog 생성 및 서버 기동 
```
jekyll new mysiteblog
cd mysiteblog
jekyll serve

```


Step8. 테스트
```
# http://localhost:4000
```

Step9. 포스트하기 
1. 파일이름은 YYYY-MM-dd-{제목}.md 형태이다.
2. Front Matter 를 작성한다.
http://jekyllrb.com/docs/frontmatter/

