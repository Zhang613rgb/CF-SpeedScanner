# CF-SpeedScanner

Cloudflare 优选 IP 扫描器。每日自动测速，筛选延迟最低的节点。

## 用法

本地运行：
```bash
python cfip.py scan -n 5 --repo . --push
```

GitHub Actions 每日自动运行（配置在 `.github/workflows/daily-speedtest.yml`）。

## 输出

`speedtest/output/cfyd.txt` — 格式：
```
IP:端口#IP-端口 [数据中心] 速度延迟
```

## 订阅接入

可配合 edgetunnel 使用：

```
&sub=https://raw.githubusercontent.com/Zhang613rgb/CF-SpeedScanner/main/speedtest/output/cfyd.txt
```
