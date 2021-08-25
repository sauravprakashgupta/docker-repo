add new user and roles in this file

/var/lib/docker/volumes/tomcat_configurations/_data/conf/tomcat-users.xml


<tomcat-users xmlns="http://tomcat.apache.org/xml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://tomcat.apache.org/xml tomcat-users.xsd" version="1.0">

<!--<user username="deployer" password="deployer" roles="manager-gui,manager-script,admin-gui"/> -->
<user username="deployer" password="deployer" roles="manager-script"/>
<user username="manager" password="" roles="manager-gui,admin-gui"/>

</tomcat-users>


========================================

comment the below mentioned lines in this mentioned file

/var/lib/docker/volumes/tomcat_data/_data/tomcat/webapps/manager/META-INF/context.xml

<Context antiResourceLocking="false" privileged="true" >
<!--  <CookieProcessor className="org.apache.tomcat.util.http.Rfc6265CookieProcessor"
                   sameSiteCookies="strict" />
  <Valve className="org.apache.catalina.valves.RemoteAddrValve"
         allow="127\.\d+\.\d+\.\d+|::1|0:0:0:0:0:0:0:1" />
  <Manager sessionAttributeValueClassNameFilter="java\.lang\.(?:Boolean|Integer|Long|Number|String)|org\.apache\.catalina\.filters\.CsrfPreventionFilter\$LruCache(?:\$1)?|java\.util\.(?:Linked)?HashMap"/> -->
</Context>
