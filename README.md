 <h1>WebRTC 点对点视频通话系统</h1>
 
 <strong>主要功能：<strong><br>
 1、基于websocket的在线用户列表；<br>
 2、用websocket作为信令通道，构建WebRTC视频通话。<br>
<span style="margin-left:50px;">-------------------------------------------------------2014-12-02<span>

开发IDE：MyEclipse 8.6
工程编码方式：UTF-8

环境要求：
    1、Tomcat 要求为7.0以上的版本

注意：
   部署时，需要将js/config.js文件中"ws://localhost:8080/"改为"ws://服务器计算机IP:端口/"。
   
出现问题及解决方法：

java.lang.NoSuchMethodException: org.apache.catalina.deploy.WebXml addServlet
          解决方法：Tomcat安装文件context.xml里的Context标签中添加<Loader delegate="true" />即可解决该问题。

java.lang.NoSuchMethodError: org.apache.catalina.connector.RequestFacade.doUpgrade(Lorg/apache/coyote/http11/upgrade/UpgradeInbound;)V
          解决方法：找到Tomcat安装文件夹中的lib文件夹，删除其中名为“catalina.jar”和“tomcat-coyote.jar”两个jar文件，将本工程中WebRoot——>WEB-INF——>lib文件夹中名为“catalina.jar”和“tomcat-coyote.jar”两个jar文件拷贝到Tomcat安装文件夹内的lib文件夹里。
