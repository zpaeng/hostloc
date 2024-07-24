# Hostloc 签到脚本
Hostloc 全球主机交流论坛 PHP刷分脚本

## 食用方法
~~1. 打开index.php，修改顶部配置部分的账号、密码、推送key等信息~~

~~2. 使用定时任务，**每小时**执行一次php文件。例：`0 * * * * php /home/www/index.php`~~
1. 利用github action定时执行，在github setting-Secrets and variables-Actions-Repository secrets-New repository secret新增【ACCOUNTS】,格式为`username1,password1;username2,password2`
2. 在Actions标签中允许`enable workflow`

## 消息推送 KEY
1. Telegram关注 @onePushBot
2. 发送/start即可获取到你的SCKEY
3. 粘贴到index.php文件中对应的位置

## Log
- 2023-07-20 修复了下签到失败的消息推送功能
- 2021-09-29 最近好久没用也没管这个脚本了，跑去用Laravel写了个多账号带面板的签到，所以如果此脚本失效，记得喊我
- 2021-05-22 HTML版本受限于新版Chrome安全策略，已经失效。可以换其他垃圾浏览器试试，或者直接使用PHP版的
- 2021-03-01 临时更新，解决签到失败问题
- 2019-07-01 优化访问随机间隔时间，且每日多次尝试，晚上9点统一推送失败账号（**所以定时任务请设置每小时执行一次php脚本**）
- 2019-03-25 论坛偶尔防CC误伤，所以增加了签到(登录)失败的推送通知

## TODO
后面考虑做一个自动签到平台，问题用户放心把账号放我这吗？显然不会，再说吧

就这样溜了
