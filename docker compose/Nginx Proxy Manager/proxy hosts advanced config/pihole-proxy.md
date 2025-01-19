location / {
      proxy_pass http://10.0.0.50:80/admin/;
      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
      proxy_hide_header X-Frame-Options;
      proxy_set_header X-Frame-Options "SAMEORIGIN";
      proxy_read_timeout 90;
    }
    location /admin {
      proxy_pass http://10.0.0.50:80/admin/;
      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
      proxy_hide_header X-Frame-Options;
      proxy_set_header X-Frame-Options "SAMEORIGIN";
      proxy_read_timeout 90;
    }
