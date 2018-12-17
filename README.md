# sspanel对应的ssr后端docker镜像

## 支持的标签
- `x86`
- `arm32v6`

## 支持的环境变量
- `NODE_ID`
- `SPEEDTEST`
- `CLOUDSAFE`
- `AUTOEXEC`
- `ANTISSATTACK`
- `MU_SUFFIX`
- `MU_REGEX`
- `API_INTERFACE`
- `WEBAPI_URL`
- `WEBAPI_TOKEN`
- `MYSQL_HOST`
- `MYSQL_PORT`
- `MYSQL_USER`
- `MYSQL_PASS`
- `MYSQL_DB`
- `REDIRECT`
- `FAST_OPEN`

## docker-compose demo
```
version: "3"

services:
  ssrmu:
    container_name: ssrmu
    hostname: ssrmu
    image: liuweijian/ssrmu:x86
    network_mode: "host"
    restart: always
    logging:
      driver: "json-file"
      options:
        max-size: "50m"
        max-file: "3"
    environment:
      - NODE_ID=10
      - API_INTERFACE=glzjinmod
      - MYSQL_HOST=xxx
      - MYSQL_USER=xx
      - MYSQL_DB=xxx
      - MYSQL_PASS=xxx
```