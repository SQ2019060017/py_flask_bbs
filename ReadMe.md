# Flask 全栈开发论坛

## 论坛功能演示
 - 密码找回
   ![forget_password](pictures/forget_password.gif)
 - 后台管理
   ![admin](pictures/admin.gif)
 - 用户信息管理
   ![user_info](pictures/user_info.gif)
 - 论坛发帖
   ![topics](pictures/topics.gif)
 - 评论@提醒功能
   ![notice](pictures/notice.gif)
 - 一键部署
   ![deploy](pictures/deploy.gif)

## 论坛功能简介：
 - 实现用户的注册、登录、验证，个人信息（如头像、昵称、签名等）的修改；
 - 个人主页实现发布话题与参与话题独立展示，并按照最新时间倒序排列；
 - 实现用户忘记密码后的密码找回功能，邮件验证；
 - 帖子的发布、删除、评论以及帖子的分板块管理；
 - 实现站内信的邮件通知功能以及评论中的@邮件提醒。

## 论坛配置优化
 - Nginx 文件内配置 HTTPS 加密传输协议，多类型文件压缩标准，反向代理，静态文件缓存时效等。
 - 利用 Redis 实现安全的服务端 Session，替换不安全的 Flask 内置 Session，通过服务器端 Session 验证用户，并实现进程共享。
 - 实现ORM性能优化，论坛数据存储使用MySQL，针对需要频繁读取的数据使用 Redis 进行缓存优化，降低路由开销。
 - 通过密码加盐处理保护用户密码安全，利用 Token 防范 XSRF 攻击。
 - 利用异步任务队列处理站内信的邮件发送，保护重要信息不被丢失，提高用户体验。
