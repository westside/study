* 검색
```
sudo apt-cache search mysql-server
```

* 5.6버전으로 설치
```
sudo apt-get install mysql-server-5.6
```

* mysql login 후 권한 설정
```
mysql -u root -p
use mysql;
GRANT ALL PRIVILEGES ON *.* to 'root'@'%' IDENTIFIED BY 'password';
flush privileges;
```

* user 추가 (// database(*).table(*)) https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql
```
CREATE USER 'user'@'%' IDENTIFIED BY 'bhaptics';
GRANT ALL PRIVILEGES ON * . * TO 'user'@'%';    
FLUSH PRIVILEGES;
```

* my.cnf 설정화일 변경
```
sudo vi /etc/mysql/my.cnf
bind-address = 127.0.0.1 이부분을 주석처리 혹은 0.0.0.0
```

* 재시작 
```
sudo /etc/init.d/mysql restart
```

* 한글 설정
```
[mysqld]

datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
character-set-server=utf8
collation-server=utf8_general_ci
init_connect = set collation_connection = utf8_general_ci
init_connect = set names utf8

 

[mysql]
default-character-set=utf8
 

[mysqld_safe]
log-error=/var/log/mysqld.log
pid-file=/var/run/mysqld/mysqld.pid
default-character-set=utf8
 

[client]
default-character-set=utf8
 
[mysqldump]
default-character-set=utf8
```

* 7) innodb 설정
```
sudo vi /etc/mysql/my.cnf에 추가

innodb_data_home_dir = /var/lib/mysql
innodb_data_file_path = ibdata1:10M:autoextend
innodb_log_group_home_dir = /var/lib/mysql
innodb_buffer_pool_size = 256M
innodb_additional_mem_pool_size = 20M
innodb_log_file_size = 64M
innodb_log_buffer_size = 8M
innodb_flush_log_at_trx_commit = 1
innodb_lock_wait_timeout = 50
```

## 참고
* sql : https://gist.github.com/westside/2c4eb0c9b553e2ca98cfa7497800498e
* 설정 파일 : https://gist.github.com/westside/f0fcfed9457fc9ab5ade0133673800d3
* http://jaesu.tistory.com/entry/ubuntu-mysql-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0
