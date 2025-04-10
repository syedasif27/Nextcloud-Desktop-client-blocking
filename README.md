# Nextcloud desktop client blocking 

To prevent desktop client from accessing Nextcloud, the following configuration will be added to the virtual host file of apache (/etc/httpd/conf.d/"your-conf-file".conf) or (/etc/apache2/sites-available/"your-config-file".conf)

        RewriteEngine On
        RewriteCond %{HTTP_USER_AGENT} "mirall" [NC]
        RewriteRule ^ - [F,L]
 
 # Web access will remain unaffected



