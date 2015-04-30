<h2>
 Redis Session Manager for Apache Tomcat
</h2>

**以下是tomcat/conf/content.xml 中的配置**

`<Valve className="com.orangefunction.tomcat.redissessions.RedisSessionHandlerValve" />
<Manager className="com.orangefunction.tomcat.redissessions.RedisSessionManager"
         host="localhost" <!-- optional: defaults to "localhost" -->
         port="6379" <!-- optional: defaults to "6379" -->
         database="0" <!-- optional: defaults to "0" -->
         maxInactiveInterval="60" <!-- optional: defaults to "60" (in seconds) -->
         sessionPersistPolicies="PERSIST_POLICY_1,PERSIST_POLICY_2,.." <!-- optional -->
         sentinelMaster="SentinelMasterName" <!-- optional -->
         sentinels="sentinel-host-1:port,sentinel-host-2:port,.." <!-- optional --> />`

**复制以下这些包(/WebContent/WEB-INF/lib)到/tomcat/lib目录中:**

commons-logging-1.1.3.jar
redis-tomcat8-session.jar
jedis-2.5.2.jar
commons-pool2-2.2.jar
tomcat-juli.jar

启动redis并启动tomcat.
