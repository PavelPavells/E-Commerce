# E-Commerce
The following steps can be taken in order to use the source code correctly. 
1) Download this project from https://github.com/PavelPavells/E-Commerce;
2) Download, Start, add folder e-commerce in htdocs;
3) Installation XAMPP:
    a) lamp/etc/extra/httpd-xampp.conf
    b) <Directory "/opt/lampp/phpmyadmin">
            AllowOverride AuthConfig Limit
          !!!  Require all granted (change and save this line and add string Require all granted)
            ErrorDocument 403 /error/XAMPP_FORBIDDEN.html.var
        </Directory>
    c) Restart Apache
    d) lamp/etc/extra/httpd-vhosts.conf 
    e) add this block down => <VirtualHost *:80>
                                ServerAdmin webmaster@e-commerce.com
                                DocumentRoot "/opt/lampp/htdocs/e-commerce"
                                ServerName e-commerce.com
                                ErrorLog "logs/e-commerce.com-error_log"
                                CustomLog "logs/e-comerce.com-access_log" common
                              </VirtualHost>
    f) lamp/etc/httpd.conf => change and delete "#"
                            before:
                                # Virtual hosts
                                #Include etc/extra/httpd-vhosts.conf
                            after:
                                # Virtual hosts
                                Include etc/extra/httpd-vhosts.conf
    g) open cosole and add this string => sudo nano /etc/hosts => enter => add this string "192.168.64.2    e-commerce.com"
        => ctrl + x => enter
    h) RESTART APACHE!!!
    i) add e-commerce.com in google search bar => enter

4) Go to e-commerce.com/phpmyadmin
5) Create a new Database named "e-commerce" 
6) In import the file ecommerce.sql to the newly created database which is in this folder.
7) Now visit e-commerce.com, and you'll see the project is working fine on your browser. 
8) All done! 

Contact me: 
    Email: hismailforyou@gmail.com
