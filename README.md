## 👋 Welcome to matrix 🚀  

matrix README  
  
## nginx config

```config
  location /_matrix {
    proxy_ssl_verify                        off;
    send_timeout                            3600;
    proxy_connect_timeout                   3600;
    proxy_send_timeout                      3600;
    proxy_read_timeout                      3600;
    proxy_http_version                      1.1;
    proxy_request_buffering                 off;
    proxy_buffering                         off;
    proxy_set_header                        Host               $host;
    proxy_set_header                        X-Real-IP          $remote_addr;
    proxy_set_header                        X-Forwarded-Proto  $scheme;
    proxy_set_header                        X-Forwarded-Scheme $scheme;
    proxy_set_header                        X-Forwarded-For    $remote_addr;
    proxy_set_header                        X-Forwarded-Port   $server_port;
    proxy_set_header                        Upgrade            $http_upgrade;
    proxy_set_header                        Connection         $connection_upgrade;
    proxy_set_header                        Accept-Encoding "";
    proxy_pass                              http://172.17.0.1:8008/_matrix;
    }
  location /_synapse {
    proxy_ssl_verify                        off;
    send_timeout                            3600;
    proxy_connect_timeout                   3600;
    proxy_send_timeout                      3600;
    proxy_read_timeout                      3600;
    proxy_http_version                      1.1;
    proxy_request_buffering                 off;
    proxy_buffering                         off;
    proxy_set_header                        Host               $host;
    proxy_set_header                        X-Real-IP          $remote_addr;
    proxy_set_header                        X-Forwarded-Proto  $scheme;
    proxy_set_header                        X-Forwarded-Scheme $scheme;
    proxy_set_header                        X-Forwarded-For    $remote_addr;
    proxy_set_header                        X-Forwarded-Port   $server_port;
    proxy_set_header                        Upgrade            $http_upgrade;
    proxy_set_header                        Connection         $connection_upgrade;
    proxy_set_header                        Accept-Encoding "";
    proxy_pass                              http://172.17.0.1:8008/_synapse;
    }
  location /.well-known/matrix {
    proxy_ssl_verify                        off;
    send_timeout                            3600;
    proxy_connect_timeout                   3600;
    proxy_send_timeout                      3600;
    proxy_read_timeout                      3600;
    proxy_http_version                      1.1;
    proxy_request_buffering                 off;
    proxy_buffering                         off;
    proxy_set_header                        Host               $host;
    proxy_set_header                        X-Real-IP          $remote_addr;
    proxy_set_header                        X-Forwarded-Proto  $scheme;
    proxy_set_header                        X-Forwarded-Scheme $scheme;
    proxy_set_header                        X-Forwarded-For    $remote_addr;
    proxy_set_header                        X-Forwarded-Port   $server_port;
    proxy_set_header                        Upgrade            $http_upgrade;
    proxy_set_header                        Connection         $connection_upgrade;
    proxy_set_header                        Accept-Encoding "";
    proxy_pass                              http://172.17.0.1:8008/.well-known/matrix;
    }

```

## Author  

🤖 casjay: [Github](https://github.com/casjay) 🤖  
