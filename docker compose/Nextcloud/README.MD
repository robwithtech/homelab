Link to Nextcloud official site https://nextcloud.com/

This container uses a macvlan that was created on the video below. It was named "local-network".

Link to my youtube video showing this nextcloud.yml file being used with openmediavault https://youtu.be/SQ80JmRQE_o

CHANGE_TO_COMPOSE_DATA_PATH is a parameter used in openmediavault to specify the default container data path.

****Parameters used on the video are below:

.../appdata/nextcloud/config/www/nextcloud/config/config.php

  'default_phone_region' => 'US',
  'memcache.local' => '\\OC\\Memcache\\APCu',
  'maintenance_window_start' => 1,

****Strict Transport Security
.../appdata/nextcloud/config/nginx/site-confs/default.conf

add_header Strict-Transport-Security "max-age=31536000; includeSubDomains" always;

****Redirect nextcloud to HTTPS
server {
    listen 80 default_server;
    server_name _;
    return 301 https://$host$request_uri;
}
