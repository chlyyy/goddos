# Help
```bash
./goddos -h
```

```bash
Usage of ./goddos:
  -cc int
        并发用户数量 (default 8000)
  -dm int
        DDos攻击持续时间（分钟） (default 20)
  -ims int
        每个用户执行DDos攻击的频率（毫秒） (default 1000)
  -m string
        DDos攻击目标URL请求方式(GET/POST/...) (default "GET")
  -u string
        DDos攻击的目标URL (default "https://www.yoursite.com")
```


# Example
```bash
./goddos -cc 1000 -u https://www.yoursite.com

// 后台运行
nohup ./goddos -cc 1000 -u https://www.yoursite.com &

// 后台运行，不写日志
nohup ./goddos -cc 8000 -u https://www.yoursite.com >/dev/null 2>&1
```



- open many files:
```bash
sudo ulimit -n 8192
```
@see https://www.jb51.net/LINUXjishu/228022.html
