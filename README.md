# tomcat_9_catalina_base_configuration_5

eso arranca el tomcat usando un CATALINA_BASE distinto de su valor per defecto, que en ese caso vale C:\apache\tomcat\catalina_bases\tomcat9_userguide_step2_v5
Está un war del ejemplo de la documentación de apache : sample.war desplegado y se puede usar el manager de tomcat para parar esa aplicación de ejemplo / volver a levantarla
url de la aplicación : http://localhost:8080/sample/
url del manager : http://localhost:8080/manager
username/password : tomcat_5/tomcat_5
El username/password está definido en el archivo ./conf/tomcat-users.xml así :
	<role rolename="manager-gui"/>
	<user username="tomcat_5" password="tomcat_5" roles="manager-gui"/>

Al arrancar tomcat, se puede ver en la url http://localhost:8080/sample/ que la página de sample aparece correctamente.

En el manager, en la tabla "Aplicaciones", a la línea con columna "Ruta" que vale "/sample", se puede clicar en el botón [Parar].
Al clicar el botón [Parar], no se puede acceder más a la página de http://localhost:8080/sample (si se puede es que hay que vacíar el cache o volver a acceder a esa url en na ventana incognito privada, o con un nuevo navegador).

Luego en el manager, en la misma línea, aparece un botón [Arrancar], al clicar en ese botón, se puede volver a ver la página de la aplicación en la misma url http://localhost:8080/sample.

