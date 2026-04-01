# gb5


https://www.apachefriends.org



https://github.com/gnuboard/gnuboard5


#win
: path : C:\xampp\mysql\bin

+ sql root 1234

sql admin -> make db g5

and import from C:\xampp\htdocs\install\gnuboard5shop.sql

mysql -u root -p

CREATE USER <usrname>;

GRANT ALL PRIVILEGES ON g5.* to '<usrname>'@'%' identified by '<password>';


# community to shop

in

theme/테마명/theme.config.php 

define('G5_COMMUNITY_USE', false);


# enable gd 

php.ini -> ;extension=gd to extension=gd

# hide  "FAQ" "Q&A" "새글" "접속자"
C:\xampp\htdocs\theme\basic\css\default.css
```
/* 상단 FAQ, Q&A, 새글, 접속자 숨기기 추가 */
#hd_define li a[href*="faq.php"], 
#hd_qnb li a[href*="faq.php"],
#hd_define li a[href*="qalist.php"], 
#hd_qnb li a[href*="qalist.php"],
#hd_define li a[href*="new.php"], 
#hd_qnb li a[href*="new.php"],
#hd_define li a[href*="current_connect.php"],
#hd_qnb li a[href*="current_connect.php"] {
    display: none !important;
}

/* 항목이 사라진 후 남는 여백(테두리나 마진) 처리 */
#hd_define li:has(a[href*="faq.php"]), 
#hd_define li:has(a[href*="qalist.php"]),
#hd_define li:has(a[href*="new.php"]),
#hd_define li:has(a[href*="current_connect.php"]),
#hd_qnb li:has(a[href*="faq.php"]), 
#hd_qnb li:has(a[href*="qalist.php"]),
#hd_qnb li:has(a[href*="new.php"]),
#hd_qnb li:has(a[href*="current_connect.php"]) {
    display: none !important;
}
```

# photo crop



#pwreset
mysql -u root -p -e "USE <dbname>; UPDATE g5_member SET mb_password = password('<new_pw>') WHERE mb_id = '<admin_id>';"
