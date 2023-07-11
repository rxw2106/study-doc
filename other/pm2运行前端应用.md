> pm2 前端应用运行工具

例 本地部署画图软件excalidraw
```text
git clone https://github.com/excalidraw/excalidraw.git
```

安装依赖
```text
yarn
```
通过pm2启动服务
```
pm2 start -n excalidraw yarn -- start
pm2 save
```
pm2开机自启
```text
pm2 startup
```