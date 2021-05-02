---
description: >-
  By default you are given 2 web sites. This page will show you how to display
  and edit those sites.
---

# How to customize sites

### Default Sites

The sites you are given are http://website1.com and http://website2.com.  
You can display these in your Windows Host file at C:\Windows\System32\drivers\etc\hosts. To see the site you add the entries like this below.

```text
3.229.122.138		website1.com
3.229.122.138		website2.com
```

Open a browser with those URLS and you will see your site with the default ColdBox frameworks. In order to set different site names you will want to edit  website1.conf and website2.conf files open a shell and navigate to:

```text
/etc/nginx/sites-enabled# ls
website1.conf  website2.conf
cat website2.conf
```

* replace all website2.com entries except the directory.

```text
###############################################################
# Example
###############################################################
server {
        ################### SERVER NAME AND PORT #####################
        listen 80;
    server_name website2.com;

        ################### LOGS #####################
        access_log /var/log/nginx/website2-access.log;
        error_log /var/log/nginx/website2-error.log warn;
        rewrite_log off;

        ################### LOCATION #####################
        root /var/www/website2;

        ################### CFML #####################
        # Mod_cfml (Lucee) specific: add a unique ID for this server block.
        # For more info, see http://www.modcfml.org/index.cfm/install/web-server-components/nginx-all-os/
        set $lucee_context "website2.com";

        set $application_port "8002";
        include lucee.conf;
}
```

* Restart the Nginx and restart the server. Open your new site.

