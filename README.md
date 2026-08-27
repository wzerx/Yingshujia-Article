# 影术家｜联网版

面向电影史研究的在线优先、离线可用学术工作台。

## 当前联网能力

- 邮箱一次性链接登录
- 任务、阅读计划、PDF书目、笔记、研究卡、论文提纲、草稿和回收站云端同步
- 本机即时保存，断网后继续编辑，恢复网络后自动同步
- 两台设备同时修改时自动三向合并，并保留冲突副本
- PDF与影片本体默认不上传，只同步书目信息和研究记录
- 本机JSON备份与WPS文稿导出

## 首次启用

1. 在 Supabase SQL Editor 运行 `supabase-init.sql`。
2. 在 Authentication → URL Configuration 中，将 Site URL 和 Redirect URL 设置为：
   `https://wzerx.github.io/Yingshujia-Article/`
3. 将 `index.html` 上传到 GitHub 仓库根目录，覆盖旧版。

## 安全边界

- 网页仅使用 Supabase Publishable Key。
- 数据表已启用 Row Level Security，用户只能访问自己的记录。
- 不要将数据库密码、Secret Key 或 service_role key 写入网页或仓库。

