# App-Center
软件中心


## 📦 最新发布 (Latest Releases)
<!-- RELEASE_TABLE_START -->
| 项目 (Project) | 版本 (Tag) | 更新时间 (Time) | 更新日志 (Log) | 下载 (Download) |
| :--- | :--- | :--- | :--- | :--- |
| CT_Translation | CT_Translation-20260831-002204-15 | 2026-08-31 00:22 | - 新增 Services/QpsRateLimiter.cs：滑动窗口限流器，线程安全，配额用完时异步等到最早的请求滑出 1 秒窗口，取消令牌可中断等待。 Models/AppConfig.cs：三个配置类各加 QpsLimit。默认值按现状取：腾讯 5（官方限制）、Google 5（等值于原来写死的 200ms 间隔）、OpenAI 0（不限，各家网关差异大）。旧 config.json 不受影响，缺省字段自动用默认值。 三个翻译服务：在每次实际发请求前 AcquireAsync 拿配额（重试也各占一个配额，因为服务端就是这么计数的）。腾讯服务删掉了原来的随机延迟——它的“碰运气”作用已被精确限流取代；Google 删掉了每批后固定睡 200ms。 设置窗口：三个服务配置区各加“QPS 限制”输入框，带说明文字；非法输入保持原值不变。 | [点击下载](https://github.com/1592363624/App-Center/releases/download/CT_Translation-20260831-002204-15/CT_Translation.zip) |
| ReOperation | AutomationAssistant-20260121-080351-3 | 2026-01-21 16:04 | - 移除AutomationAssistant.sln.DotSettings.user文件<br>- ci: 更新触发打包工作流中的目标仓库名称<br>- 添加 GitHub Actions 工作流<br>- 添加 GitHub Actions 工作流<br>- 添加 GitHub Actions 工作流 | [点击下载](https://github.com/1592363624/App-Center/releases/download/AutomationAssistant-20260121-080351-3/ReOperation.zip) |
| SteamAccountManager | AutomationAssistant-20260121-080351-3 | 2026-01-21 16:04 | - 移除AutomationAssistant.sln.DotSettings.user文件<br>- ci: 更新触发打包工作流中的目标仓库名称<br>- 添加 GitHub Actions 工作流<br>- 添加 GitHub Actions 工作流<br>- 添加 GitHub Actions 工作流 | [点击下载](https://github.com/1592363624/App-Center/releases/download/AutomationAssistant-20260121-080351-3/SteamAccountManager.zip) |
<!-- RELEASE_TABLE_END -->
