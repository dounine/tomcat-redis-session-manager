<h2>
 Redis Session Manager for Apache Tomcat
</h2>
<br/>
<hr/>
**以下是tomcat/conf/content.xml 中的配置**
<br/>
`<Valve className="com.orangefunction.tomcat.redissessions.RedisSessionHandlerValve" />
<br/>
<Manager className="com.orangefunction.tomcat.redissessions.RedisSessionManager"<br/>
         host="localhost" <!-- optional: defaults to "localhost" --><br/>
         port="6379" <!-- optional: defaults to "6379" --><br/>
         database="0" <!-- optional: defaults to "0" --><br/>
         maxInactiveInterval="60" <!-- optional: defaults to "60" (in seconds) --><br/>
         sessionPersistPolicies="PERSIST_POLICY_1,PERSIST_POLICY_2,.." <!-- optional --><br/>
         sentinelMaster="SentinelMasterName" <!-- optional --><br/>
         sentinels="sentinel-host-1:port,sentinel-host-2:port,.." <!-- optional --> />`<br/>
<br/>
<hr/>
**复制以下这些包(/WebContent/WEB-INF/lib)到/tomcat/lib目录中:**
<br/>
commons-logging-1.1.3.jar<br/>
redis-tomcat8-session.jar<br/>
jedis-2.5.2.jar<br/>
commons-pool2-2.2.jar<br/>
tomcat-juli.jar<br/>
<br/>
启动redis并启动tomcat.<br/>