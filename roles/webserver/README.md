# Webserver Role

Servs prometheus and grafana

default vars:

```yml
monitoring_nginx_config_path: "/opt/nginx/configs"

prometheus_nodeport: 30090
prometheus_domain: "prom.noorbala7418.ir"
prometheus_login_user: "admin"
prometheus_login_password: "admin1234"
prometheus_password_file_path: "{{ monitoring_nginx_config_path  }}/.htpasswd"

grafana_nodeport: 30030
grafana_domain: "grafana.noorbala7418.ir"

```