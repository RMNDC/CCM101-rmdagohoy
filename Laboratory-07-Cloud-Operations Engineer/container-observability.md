# Container Observability

## Application Logs
2026/10/10 04:43:51 [error] 29#29: *4 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"
172.17.0.1 - - [10/Oct/2026:04:43:51 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"

Application logs are vital for troubleshooting because they show exactly what went wrong and where errors occur. Without them, finding and fixing broken links or missing files in your application would be mostly guesswork.

## Container Metrics

| Metric | Value |
|---|---|
| Container | client-website |
| CPU usage | 0.00% |
| Memory usage | 2.699MiB |

