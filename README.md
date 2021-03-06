# Chat-App-Online
本项目实现了一个即时聊天软件，能够登录、注册、群聊、私聊、添加好友、分组展示、删除好友等，聊天消息支持文字、图片、文件，使用的flask和flask-sockets进行开发。

本项目以 https://www.heanny.cn/post-487.html 这位博主实现的FLASK WEBSOCKET聊天室为基础，对Server部分和客户端的页面等进行了改写，添加了注册、登录页面，增加了数据库的设计，增加了好友分组、添加好友、好友验证、删除好友等功能。时间有限，存在部分不合逻辑的地方和有待修复的bug。

#### 技术实现
后台框架使用的Flask框架，通信使用了flask-Sockets、HTTP等协议，数据库使用的Mongo。

#### 功能介绍
1. 简单的登录注册
2. 公共大厅聊天、好友私聊（支持文字、图片、文件）
3. 添加好友
4. 删除好友
5. 好友分组

#### 运行方法
1. pip3 install -r requirements.txt
2. cd chat_web && python3 run.py
3. cd server && python3 run.py

#### 有待改善的部分
1. 注册页面存在注册失败依然弹出注册成功的弹窗的情况（弹出后跳转错误页面）
2. 头像为注册时随机生成的
3. 用户无法得知自己的ID，没有在页面上做展示
4. 好友请求需要重新登录才能看到提示，没有实现在线的提示（是否有待处理的好友请求是在登录时进行判断的）
5. 确认编辑标签后会自动跳转到大厅聊天
6. index.js中的代码存在冗余，混用了多种通信协议，略显杂乱（js太菜）
7. 没有保存历史聊天记录

#### 运行图示
注册
![image](https://github.com/massive11/Chat-App-Online/blob/master/readme_imgs/register.png)

登录
![image](https://github.com/massive11/Chat-App-Online/blob/master/readme_imgs/login.png)

搜索
![image](https://github.com/massive11/Chat-App-Online/blob/master/readme_imgs/search.png)

分组展示和聊天示意
![image](https://github.com/massive11/Chat-App-Online/blob/master/readme_imgs/chat.png)