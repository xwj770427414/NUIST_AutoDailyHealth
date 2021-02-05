# NUIST_AutoDailyHealth
基于Python3.8和Selenium的南信大健康日报自动化脚本
## 环境配置
- Python3.X
- selenium
- Chrome
- ChromeDriver(与Chrome版本需对应，镜像：http://npm.taobao.org/mirrors/chromedriver/)
## 功能
- 自动输入账户密码登录
- 自动填报
- 可利用简单定时任务每日自动填报
## 运行
- 将ChromeDriver添加进Path
- 更改Auto_DailyHealth.py中的登录信息
- 运行脚本
## 局限
- 校网站不稳定，偶见无法登陆造成填报失败
- 未添加登录结果反馈
