# squirrelAI


## 项目说明

----
<table>

<tr>
<td>产品名称：</td>
<td>松鼠AI</td>
<td>版本：</td>
<td>V 2.2</td>
</tr>

<tr>
<td>作者：</td>
<td>张益斌</td>
<td>更新日期：</td>
<td>2018/10/13</td>
</tr>

</table>


#### 一、制作背景

Im Zeitalter der Im-Proliferation wird die Kommunikation zwischen den Menschen immer bequemer, und man hat immer weniger Zeit und Raum für sich selbst. Jeden Tag sind Sie mit der Arbeit und dem Leben beschäftigt, und gleichzeitig müssen Sie eine Menge Energie aufwenden, um Nachrichten aus verschiedenen Szenarien zu bearbeiten.
Möchten Sie innehalten und eine Weile allein sein, ohne Anrufe oder Nachrichten, und "die Welt für einen Moment für sich spüren"?
WeChat ist aus dem Leben der chinesischen Nutzer nicht mehr wegzudenken; der größte Vorteil besteht darin, dass es die Menschen durch Peer-to-Peer-Instant-Messaging näher zusammenbringt. Diese Bequemlichkeit hat jedoch auch ein neues Problem mit sich gebracht: die "soziale Angst".
Squirrel AI ist ein Tool, das Ihnen helfen kann, die meisten Nachrichten zu bearbeiten, die Sie für unwichtig halten, ohne dabei zu "höflich" zu sein; und durch die Technologie der "Turing-Bots" kann es Ihnen auch mehr Gesellschaft in Ihrem Leben bieten.
![image](./image/squirrelAI.png)

Beispiel für die Nachricht:<br
! [image](. /image/msg.png)

#### II. Vielen Dank für Ihre Spende

Wenn Sie denken, dass "Squirrel Ai" ein interessantes Programm ist, und wenn Sie die Absicht haben, zu spenden, spenden Sie bitte an:<br>
1. alipay-Konto: 13067760265 <br>
2) WeChat-Nummer: zhyblx<br>
3. die Kartennummer der China Merchants Bank: 6214 8557 1279 0845<br>
4. die Kartennummer der Ping An Bank: 623058 000018 3696983<br>

Vielen Dank an die Einzelpersonen und Unternehmen, die gespendet haben.
<table>

<tr>
<td>Datum der Spende</td
<td>Name des Unternehmens (/der Einzelperson)</td
<td>Spendenbetrag</td
</tr>

<tr>
<td>2018-12-15</td
<td>Zhi Rang Händler für Dekorationsmaterial, Hangzhou Jiahao Jia Meiju Einkaufszentrum für Dekorationsmaterial</td
<td>¥500.0</td
</tr>

</table>



#### III. Prozessgestaltung

! [image](. /image/image.png)


#### IV. Schnittstellenbeschreibung

Das gesamte Squirrel AI-Projekt ist in zwei Schichten unterteilt: die Funktionsschicht und die Nutzungsschicht. <br>

*Funktionsschicht:<br

Die funktionale Schicht als Ganzes ist in drei Teile unterteilt, und zwar in die Entwurfsschicht (Basisschicht), die Anwendungsschicht (Anwendungsschicht) und die Funktionsschicht (AI-Funktionsschicht). <br>

a)foundation(基础层):
<table>
<tr>
<td>功能</td>
<td>包</td>
<td>类</td>
<td>方法</td>
<td>参数</td>
<td>返回类型</td>
<td>描述</td>
</tr>
    
<tr>
<td>接口定义</td>
<td>com.zhangyibin.foundation.wechatinterface;</td>
<td>WechatInterface</td>
<td>/</td>
<td>/</td>
<td>/</td>
<td>定义常量</td>
</tr>
    
<tr>
<td>获取UUID</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>getUUID()</td>
<td>/</td>
<td>String</td>
<td>微信登录的唯一识别信息</td>
</tr>

<tr>
<td>登录二维码</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>showQrCode()</td>
<td>/</td>
<td>/</td>
<td>获取登录二维码</td>
</tr>

<tr>
<td>展示二维码</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>QRCodeFrame</td>
<td>QRCodeFrame()</td>
<td>filePath:二维码图片地址</td>
<td>/</td>
<td>二维码通过窗体展示</td>
</tr>

<tr>
<td>登录等待</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>waitForLogin() ()</td>
<td>/</td>
<td>/</td>
<td>扫描二维码登录验证</td>
</tr>

<tr>
<td>登录等待</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>login()</td>
<td>/</td>
<td>boolean</td>
<td>登录成功返回true</td>
</tr>

<tr>
<td>初始化</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>wxInit()</td>
<td>/</td>
<td>boolean</td>
<td>初始化异常：返回false;作用于验证账号是否为微信黑名单</td>
</tr>

<tr>
<td>状态通知</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>wxStatusNotify()</td>
<td>/</td>
<td>boolean</td>
<td>状态通知监控异常：返回false;</td>
</tr>

<tr>
<td>获取好友列表</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>getContact()</td>
<td>/</td>
<td>boolean</td>
<td>好友列表获取失败:返回false;</td>
</tr>

<tr>
<td>监控消息</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>syncCheck()</td>
<td>/</td>
<td>int</td>
<td>作用于是否获取到好友消息内容</td>
</tr>

<tr>
<td>发送消息</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>webwxsendmsg()</td>
<td>
String content:消息内容
String to：接收好友
</td>
<td>/</td>
<td>处理消息发送</td>
</tr>

<tr>
<td>最新消息</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>webwxsync()</td>
<td>/</td>
<td>JSON</td>
<td>获取消息内容</td>
</tr>

<tr>
<td>回复消息</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>handleMsg()</td>
<td>JSONObject data:消息内容</td>
<td>/</td>
<td>实现给予好友消息回复</td>
</tr>

<tr>
<td>用户备注名</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>getUserRemarkName()</td>
<td>String id:微信ID</td>
<td>String</td>
<td>获取到好友备注名称</td>
</tr>

<tr>
<td>监听程序</td>
<td>com.zhangyibin.foundation.wechatapp;</td>
<td>WechatApp</td>
<td>listenMsgMode()</td>
<td>/</td>
<td>/</td>
<td>保持网络连接</td>
</tr>

<tr>
<td>好友通讯录</td>
<td>com.zhangyibin.foundation.util;</td>
<td>AddressBook</td>
<td>getAddressBookList()</td>
<td>JSONObject jsonObject:好友列表JSON</td>
<td>/</td>
<td>
1.获取好友列表<br>
2.新好友插入到数据库中
</td>
</tr>

<tr>
<td>Cookie信息</td>
<td>com.zhangyibin.foundation.util;</td>
<td>CookieUtil</td>
<td>getCookie()</td>
<td>HttpRequest request:Http请求</td>
<td>String</td>
<td>模拟浏览器Cookie信息</td>
</tr>


<tr>
<td>匹配器</td>
<td>com.zhangyibin.foundation.util;</td>
<td>Matchers</td>
<td>match()</td>
<td>
String p :正则表达
String str：匹配字符串
</td>
<td>String</td>
<td>用于处理登陆微信过程的正则表达式的处理</td>
</tr>

<tr>
<td>连接(创建)数据库</td>
<td>com.zhangyibin.foundation.databaseservice;</td>
<td>CreateSQLiteService</td>
<td>main()</td>
<td>/</td>
<td>/</td>
<td>连接(创建)数据库</td>
</tr>

<tr>
<td>message数据插入库</td>
<td>com.zhangyibin.foundation.databaseservice;</td>
<td>InsertService</td>
<td>getInsertService()</td>
<td>
String date:日期
String name：用户名
String message：消息内容
</td>
<td>/</td>
<td>消息插入数据库</td>
</tr>

<tr>
<td>message数据插入库</td>
<td>com.zhangyibin.foundation.databaseservice;</td>
<td>InsertService</td>
<td>getInsertService()</td>
<td>
String strSql:完整的SQL语句
</td>
<td>/</td>
<td>消息插入数据库</td>
</tr>

<tr>
<td>查询服务</td>
<td>com.zhangyibin.foundation.databaseservice;</td>
<td>SelectService</td>
<td>getSelectService()</td>
<td>
String sql:完整的select语句
</td>
<td>/</td>
<td>数据查询</td>
</tr>

</table>


b)application(应用层):

<table>
<tr>
<td>功能</td>
<td>包</td>
<td>类</td>
<td>方法</td>
<td>参数</td>
<td>返回类型</td>
<td>描述</td>
</tr>

<tr>
<td>特殊账号枚举</td>
<td>com.zhangyibin.application.specialusers;</td>
<td>SpecialUsersEnum</td>
<td>getNameList()</td>
<td>/</td>
<td>String</td>
<td>账号枚举列表类(不回复消息名单)</td>
</tr>

<tr>
<td>枚举值转化成List</td>
<td>com.zhangyibin.application.speciauserslist;</td>
<td>SpecialUsersList</td>
<td>getSpecialUsersList()</td>
<td>/</td>
<td>List<String></td>
<td>账号枚举列表类(不回复消息名单)</td>
</tr>

<tr>
<td>启动程序入口</td>
<td>com.zhangyibin.application;</td>
<td>StartWechatApp</td>
<td>GETStartWechatApp</td>
<td>/</td>
<td>/</td>
<td>执行程序主入口</td>
</tr>

</table>


c)aifunction(AI功能层):

<table>
<tr>
<td>功能</td>
<td>包</td>
<td>类</td>
<td>方法</td>
<td>参数</td>
<td>返回类型</td>
<td>描述</td>
</tr>

<tr>
<td>机器人调用</td>
<td>com.zhangyibin.aifunction;</td>
<td>SquirrelAiRobot</td>
<td>SquirrelRobot()</td>
<td>String msg:消息内容</td>
<td>String</td>
<td>调用图灵机器人接口(不回复消息名单)</td>
</tr>

</table>


*使用层：<br>

使用层整体分为两部分进行设计test(测试)、use(使用层)。<br>

<table>
<tr>
<td>功能</td>
<td>包</td>
<td>类</td>
<td>方法</td>
<td>参数</td>
<td>返回类型</td>
<td>描述</td>
</tr>

<tr>
<td>测试代码</td>
<td>com.squirrelAi.test;</td>
<td>/</td>
<td>/</td>
<td>/</td>
<td>/</td>
<td>工程测试代码</td>
</tr>

<tr>
<td>启动松鼠AI</td>
<td>com.squirrelAi.use;</td>
<td>UseSquirrelAi</td>
<td>main</td>
<td>/</td>
<td>/</td>
<td>启动松鼠AI,调用StartWechatApp功能</td>
</tr>

</table>


#### 四、版本管理

<table>

<tr>
<td>日期</td>
<td>版本号</td>
<td>更新内容</td>
<td>备注</td>
</tr>

<tr>
<td>2018.06.18</td>
<td>V1.0</td>
<td>
功能上线
</td>
<td>web框架：blade-kit-1.2.9-alpha.jar</td>
</tr>

<tr>
<td>2018.08.03</td>
<td>V1.1</td>
<td>

a) Basisteil:<br
Implementierung einer WeChat-Imitation durch Scannen des QR-Codes des Kunden zur Anmeldung. <br>
Stellen Sie fest, dass sich das IOS-Gerät normal anmelden kann. <br>
Implementieren, um die Kontakte aus dem WeChat-Adressbuch zu erhalten. <br>
Implementieren, um Nachrichten von WeChat-Kontakten abzuhören. <br>
Implementieren Sie beantwortbare Freundschaftsnachrichten. <br>

b) Sitzungsfunktion:<br>
Implementieren Sie den Zugangs-Bot, um auf Nachrichten von Freunden zu antworten. <br>
Implementierung einer Blacklist-Funktion zum Blockieren von Antworten auf Buddy-Nachrichten. <br>
Die Funktion der schwarzen Liste umfasst das Blockieren von persönlichen, Chatgruppen- und öffentlichen Nachrichten von Freunden. <br>
Deaktivieren Sie die automatische Bot-Antwort und wechseln Sie zur manuellen Beantwortung der Nachrichten von Freunden. <br>

c) Erweiterte Funktionalität:<br>
Ermöglicht das lokale Speichern von Chat-Nachrichten. <br>
Implementieren Sie Testprogramm-Paketierung, Debugging kann Desktop ausgeführt werden. <br>

</td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr>

<tr>
<td>2018.08.16</td
<td>V1.2</td
<td>
Fügen Sie eine Whitelist-Funktionalität hinzu, um zwischen wichtigen Freunden, die eine manuelle Antwort auf Nachrichten geben, und unwichtigen Freunden, die eine Bot-Antwort auf Nachrichten geben, unterscheiden zu können. <br>
</td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr

<tr>
<td>2018.09.28</td
<td>V2.0</td
<td>Ersetzung von JDK11<br> </td
<td>Web-Framework: blade-kit-1.2.9-alpha.jar</td
</tr>

<tr>
<td>2018.10.12</td
<td>V2.1</td
<td 
1. umbenanntes Projekt: Eichhörnchen-KI.<br 
2. Code-Refactoring; funktionale Schicht unterteilt in drei Teile: Basisschicht, Anwendungsschicht, AI-Funktionsschicht. <br
3. der Zugang zu Datenbankdiensten, die vollständige Speicherung von Nachrichten. <br>
4. ersetzen Sie das Web-Framework: blade-kit-1.3.4.jar

</td
<td
1. Web-Framework: blade-kit-1.3.4.jar<br>
2.JDBC: sqlite-jdbc-3.21.0.jar<br>
</td
</tr


<tr>
<td>2018.10.28</td
<td>V2.2</td
<td 
Aktualisierungen:<br>
Implementiert, um neue Freunde in die Datenbank aufzunehmen.
</td
<td>
--
</td
</tr>

</table>

Lokale Sicherung: /home/zhangyibin/documentation/Squirrel AI Sicherungsliste



