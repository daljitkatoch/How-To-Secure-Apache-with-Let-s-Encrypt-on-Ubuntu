# How to Install Let's Encrypt SSL Certificate

**A step-by-step guide on how you can Install the Let’s Encrypt SSL certificate**

1. First verify that lets encrypt is installed on server. 

2. Then try to installed it first with **sudo certbot --apache** and select the number appear in front of domain name list and enter.

3. If the above command not able to verify the domain for ssl then you can try the below command to install is manually.

4. Run this : **sudo certbot certonly --server https://acme-v02.api.letsencrypt.org/directory --manual --preferred-challenges dns -d 'website.com,*.website.co.uk'**

5. The above command will provide you token string two times. Enter that string in the Domain panel TXT record with **_acme-challenge** subdomain and add token in value.

6. Then Verify txt record with tool **https://toolbox.googleapps.com/apps/dig/#TXT/_acme-challenge.website.com**. Enter domain in place of **website.com** if record apears same as you entered. Then click on continue in ssh screen.

7. Restart server after this using **sudo service apache2 restart**

8. Now check website works with https://

