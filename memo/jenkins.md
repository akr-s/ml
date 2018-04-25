# Jenkins
## install CentOS7

``` bash
yum update -y
wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo
rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
sudo yum install jenkins
systemctl start jenkins
```
ブラウザでアクセスする  
http://localhost:8080/

初回アクセス時だけパスワードを要求される。  
下記ファイルの内容をコピペすれば良い。  
/var/lib/jenkins/secrets/initialAdminPassword

以降。画面の指示に従ってインストールする。


## ファイヤーウォールの設定
```
sudo firewall-cmd --permanent --zone public --add-port 8080/tcp
sudo firewall-cmd --reload
```
## 起動
```
systemctl start jenkins
```
