# log4j2

For mail set up, 

Use this https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-as-a-send-only-smtp-server-on-ubuntu-14-04
and http://sharadchhetri.com/2013/03/06/how-to-change-smtp-port-number-25-in-postfix/

1. 
sudo apt-get install mailutils

2. vi /etc/postfix/master.cf
smtp inet n – n – – smtpd

change smtp word to your desired port no. Here I am changing it to 9627

9627 inet n – n – – smtpd
3. /etc/init.d/postfix restart

4. netstat -tanp|grep 9627

5. make sure the server works 
echo "This is the body of the email" | mail -s "This is the subject line" dqx0915@hotmail.com

6. mvn pakcage and mvn exec::java to check if you receive any message
