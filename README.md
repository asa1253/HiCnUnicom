> 中国联通APP登录 签到 金币 任务 解流量封顶    [联通用户TG交流群](https://t.me/HiCnUnicom)
新增使用github自动运行，无需自己的服务器
教程：  

1、Fork 本仓库

2、在你 Fork 的仓库下的 Settings -> Secrets 页面追加以下几个secret秘密环境变量
变量名	      含义	
HAOMA  要签到的手机号码
MM     手机号码的服务密码
APPID  为联通app抓包的appd值，最好自己抓包，不会抓包就默认填 db5c52929cc2d7f5c46272487e926aebfb82b3bad6b9cd07f1eb99b6a6f34a90  <不保证这个appid能用，所以最好自己抓包>

有多个手机号码则可以自己修改仓库文件 .github/workflows/签到.yml 中的每个号码的
${{ secrets.HAOMA }}为${{ secrets.HAOMA2 }}、${{ secrets.HAOMA3 }}等等，密码同理为${{ secrets.MM }}、${{ secrets.MM2 }}
同时也需要添加Secrets变量HAOMA2、HAOMA3、MM2等等。

运行开始时间也可以自己修改.github/workflows/签到.yml文件中- cron: 05 23 * * *，你想运行的北京时间减8就行了。05代表5分，23代表23时，就是0时区23：05的意思。

ps：我自己是7个号码签到，所以.github/workflows/签到.yml文件里面有“Run 号码1-7” 7个项目，你们可以根据自己需求自由复制或者删除。

#### 各版本使用教程  
> [**CnUnicom.sh**](https://github.com/mixool/HiCnUnicom/blob/master/tutorial/CnUnicom_sh_readme.md)  
> [**UnicomGetCoin.py**](https://github.com/mixool/HiCnUnicom/blob/master/tutorial/UnicomAutoGetCoin_py_readme.md)  
  
