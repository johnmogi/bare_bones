https://medium.com/@etiennerouzeaud/play-databases-with-adminer-and-docker-53dc7789f35f

enter default user create:
https://medium.com/tech-learn-share/docker-mysql-access-denied-for-user-172-17-0-1-using-password-yes-c5eadad582d3

<pre>
docker exec -it 9051637c5174  mysql -uroot -p
mysql> CREATE USER 'john'@'172.18.0.3' IDENTIFIED BY 'password';
mysql> GRANT ALL PRIVILEGES ON *.* TO 'john'@'172.18.0.3' WITH GRANT OPTION;
mysql> flush privileges; 
mysql> exit
</pre>

in the above example the default user is - john with 'password'
