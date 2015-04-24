# desarrollo3
pommodel
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<parent>
		<artifactId>seprnp</artifactId>
		<groupId>mx.gob.sep</groupId>
		<version>0.1-SNAPSHOT</version>
	</parent>

	<groupId>mx.gob.sep.model</groupId>
	<artifactId>model</artifactId>
	<packaging>war</packaging>

	<name>model</name>

	<dependencies>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-core</artifactId>
		</dependency>
		<dependency>
			<groupId>org.apache.commons</groupId>
			<artifactId>commons-lang3</artifactId>
		</dependency>
		<!-- <dependency> <groupId>mx.gob.sep.commons</groupId> <artifactId>commons</artifactId> 
			<version>${project.version}</version> </dependency> -->
	</dependencies>

	<build>

		<resources>
			<resource>
				<directory>src/main/resources</directory>
				<filtering>true</filtering>
			</resource>
		</resources>

		<plugins>
			<plugin>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.0</version>
				<configuration>
					<source>${maven.compiler.source}</source>
					<target>${maven.compiler.target}</target>
					<encoding>UTF-8</encoding>
				</configuration>
			</plugin>
			<plugin>
				<artifactId>maven-war-plugin</artifactId>
				<version>2.3</version>
				<configuration>
					<attachClasses>true</attachClasses>
					<archiveClasses>false</archiveClasses>
					<failOnMissingWebXml>false</failOnMissingWebXml>
				</configuration>
			</plugin>
		</plugins>

	</build>

</project>

pomcommons

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<parent>
		<artifactId>seprnp</artifactId>
		<groupId>mx.gob.sep</groupId>
		<version>0.1-SNAPSHOT</version>
	</parent>

	<groupId>mx.gob.sep.commons</groupId>
	<artifactId>commons</artifactId>
	<packaging>war</packaging>

	<name>commons</name>

	<dependencies>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit-dep</artifactId>
			<scope>test</scope>
		</dependency>
		<!-- <dependency> <groupId>org.hibernate</groupId> <artifactId>hibernate-core</artifactId> 
			</dependency> -->
		<dependency>
			<groupId>log4j</groupId>
			<artifactId>log4j</artifactId>
		</dependency>


		<dependency>
			<groupId>mx.gob.sep.model</groupId>
			<artifactId>model</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>

		<dependency>
			<groupId>org.apache.httpcomponents</groupId>
			<artifactId>httpclient</artifactId>
		</dependency>

		<dependency>
			<groupId>org.apache.httpcomponents</groupId>
			<artifactId>httpmime</artifactId>
		</dependency>
		<dependency>
			<groupId>commons-io</groupId>
			<artifactId>commons-io</artifactId>
		</dependency>

		<!-- <dependency> <groupId>java</groupId> <artifactId>plugin</artifactId> 
			</dependency> -->
		<dependency>
			<groupId>com.google.code.gson</groupId>
			<artifactId>gson</artifactId>
		</dependency>


		<!-- TEST DEPENDENCIES -->
		<dependency>
			<groupId>javassist</groupId>
			<artifactId>javassist</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-core</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-beans</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-orm</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-jdbc</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context-support</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-jms</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-test</artifactId>
			<scope>test</scope>
		</dependency>

		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-core</artifactId>
		</dependency>

		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-annotations</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>javax.jms</groupId>
			<artifactId>jms</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>com.oracle</groupId>
			<artifactId>ojdbc6</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.slf4j</groupId>
			<artifactId>slf4j-log4j12</artifactId>
			<scope>test</scope>
		</dependency>

	</dependencies>

	<build>

		<resources>
			<resource>
				<directory>src/main/resources</directory>
				<filtering>true</filtering>
			</resource>
		</resources>

		<plugins>
			<plugin>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.0</version>
				<configuration>
					<source>${maven.compiler.source}</source>
					<target>${maven.compiler.target}</target>
				</configuration>
			</plugin>
			<plugin>
				<artifactId>maven-war-plugin</artifactId>
				<version>2.3</version>
				<configuration>
					<attachClasses>true</attachClasses>
					<archiveClasses>false</archiveClasses>
					<failOnMissingWebXml>false</failOnMissingWebXml>
				</configuration>
			</plugin>
		</plugins>

	</build>

</project>
pomnoti

<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<parent>
		<artifactId>seprnp</artifactId>
		<groupId>mx.gob.sep</groupId>
		<version>0.1-SNAPSHOT</version>
	</parent>

	<groupId>mx.gob.sep.ws</groupId>
	<artifactId>ws-notificaciones</artifactId>
	<packaging>war</packaging>

	<name>ws-notificaciones</name>
	<url>http://www.sep.gob.mx</url>

	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.0</version>
				<configuration>
					<source>${maven.compiler.source}</source>
					<target>${maven.compiler.target}</target>
				</configuration>
			</plugin>
		</plugins>
		<resources>
			<resource>
				<directory>src/main/resources</directory>
				<filtering>true</filtering>
				<includes>
					<include>**/*.xml</include>
					<include>**/*.properties</include>
				</includes>
			</resource>
		</resources>
	</build>

	<dependencies>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>mx.gob.sep.rnm</groupId>
			<artifactId>mailsender</artifactId>
			<version>0.1-SNAPSHOT</version>
		</dependency>
		<dependency>
			<groupId>mx.gob.sep.model</groupId>
			<artifactId>model</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>mx.gob.sep.commons</groupId>
			<artifactId>commons</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>mx.gob.sep</groupId>
			<artifactId>client-layout</artifactId>
		</dependency>
		<dependency>
			<groupId>cglib</groupId>
			<artifactId>cglib-nodep</artifactId>
		</dependency>

		<dependency>
			<groupId>commons-collections</groupId>
			<artifactId>commons-collections</artifactId>
		</dependency>

		<dependency>
			<groupId>commons-logging</groupId>
			<artifactId>commons-logging</artifactId>
		</dependency>

		<dependency>
			<groupId>dom4j</groupId>
			<artifactId>dom4j</artifactId>
		</dependency>
		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-core</artifactId>
		</dependency>

		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-annotations</artifactId>
		</dependency>

		<dependency>
			<groupId>javax.transaction</groupId>
			<artifactId>jta</artifactId>
		</dependency>

		<dependency>
			<groupId>com.oracle</groupId>
			<artifactId>ojdbc6</artifactId>
		</dependency>
		<dependency>
			<groupId>log4j</groupId>
			<artifactId>log4j</artifactId>
		</dependency>
		<dependency>
			<groupId>xml-apis</groupId>
			<artifactId>xml-apis</artifactId>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>javassist</groupId>
			<artifactId>javassist</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-core</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-beans</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-orm</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-jdbc</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context-support</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-web</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-test</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.slf4j</groupId>
			<artifactId>slf4j-log4j12</artifactId>
		</dependency>
	</dependencies>

</project>
pom fileprocess

<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<parent>
		<artifactId>seprnp</artifactId>
		<groupId>mx.gob.sep</groupId>
		<version>0.1-SNAPSHOT</version>
	</parent>

	<groupId>mx.gob.sep.process</groupId>
	<artifactId>fileprocess</artifactId>
	<packaging>ejb</packaging>

	<name>fileprocess</name>
	<url>http://www.sep.gob.mx</url>
	<build>
		<plugins>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-ejb-plugin</artifactId>
				<version>2.3</version>
				<configuration>
					<ejbVersion>3.0</ejbVersion>
					<archive>
						<index>true</index>
						<manifest>
							<addClasspath>true</addClasspath>
						</manifest>
						<manifestEntries>
							<mode>development</mode>
							<url>${project.url}</url>
							<key>value</key>
						</manifestEntries>
					</archive>
				</configuration>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.0</version>
				<configuration>
					<source>${maven.compiler.source}</source>
					<target>${maven.compiler.target}</target>
				</configuration>
			</plugin>
		</plugins>
		<resources>
			<resource>
				<directory>src/main/resources</directory>
				<filtering>true</filtering>
				<includes>
					<include>**/*.xml</include>
					<include>**/*.properties</include>
				</includes>
			</resource>
		</resources>
	</build>

	<dependencies>
		<dependency>
			<groupId>mx.gob.sep.commons</groupId>
			<artifactId>commons</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<scope>test</scope>
		</dependency>

		<dependency>
			<groupId>commons-logging</groupId>
			<artifactId>commons-logging</artifactId>
		</dependency>

		<dependency>
			<groupId>log4j</groupId>
			<artifactId>log4j</artifactId>
		</dependency>
		<!-- Javaee API -->

			<dependency>
				<groupId>javax</groupId>
				<artifactId>javaee-api</artifactId>
				<version>6.0</version>
				<scope>provided</scope>
			</dependency>


		</dependencies>

</project>

#weblogicwebapp
<?xml version="1.0" encoding="UTF-8"?>
<wls:weblogic-web-app
	xmlns:wls="http://xmlns.oracle.com/weblogic/weblogic-web-app"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://java.sun.com/xml/ns/javaee
 http://java.sun.com/xml/ns/javaee/ejb-jar_3_0.xsd
 http://xmlns.oracle.com/weblogic/weblogic-web-app
 http://xmlns.oracle.com/weblogic/weblogic-web-app/1.2/weblogic-web-app.xsd">
	<wls:weblogic-version>10.3.4</wls:weblogic-version>
	<wls:context-root>rnpportal</wls:context-root>
	<wls:container-descriptor>
		<wls:save-sessions-enabled>true</wls:save-sessions-enabled>
		<wls:prefer-web-inf-classes>true</wls:prefer-web-inf-classes>
	</wls:container-descriptor>
	
	<wls:library-ref>
		<wls:library-name>model</wls:library-name>
	</wls:library-ref>

	<wls:library-ref>
		<wls:library-name>commons</wls:library-name>
	</wls:library-ref>
</wls:weblogic-web-app>

pomaplicativos

<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<parent>
		<artifactId>seprnp</artifactId>
		<groupId>mx.gob.sep</groupId>
		<version>0.1-SNAPSHOT</version>
	</parent>

	<groupId>mx.gob.sep.ws</groupId>
	<artifactId>ws-aplicativos</artifactId>
	<packaging>war</packaging>

	<name>ws-aplicativos</name>
	<url>http://www.sep.gob.mx</url>

	<build>

		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.0</version>
				<configuration>
					<source>${maven.compiler.source}</source>
					<target>${maven.compiler.target}</target>
				</configuration>
			</plugin>
		</plugins>
	</build>

	<dependencies>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<scope>test</scope>
		</dependency>

		<dependency>
			<groupId>mx.gob.sep.model</groupId>
			<artifactId>model</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>mx.gob.sep.commons</groupId>
			<artifactId>commons</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>cglib</groupId>
			<artifactId>cglib-nodep</artifactId>
		</dependency>

		<dependency>
			<groupId>commons-collections</groupId>
			<artifactId>commons-collections</artifactId>
		</dependency>

		<dependency>
			<groupId>commons-logging</groupId>
			<artifactId>commons-logging</artifactId>
		</dependency>

		<dependency>
			<groupId>dom4j</groupId>
			<artifactId>dom4j</artifactId>
		</dependency>
		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-core</artifactId>
		</dependency>

		<dependency>
			<groupId>javax.transaction</groupId>
			<artifactId>jta</artifactId>
		</dependency>

		<dependency>
			<groupId>com.oracle</groupId>
			<artifactId>ojdbc6</artifactId>
		</dependency>
		<dependency>
			<groupId>log4j</groupId>
			<artifactId>log4j</artifactId>
		</dependency>
		<dependency>
			<groupId>xml-apis</groupId>
			<artifactId>xml-apis</artifactId>
			<scope>provided</scope>
		</dependency>

		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-core</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-beans</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-orm</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-jdbc</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context-support</artifactId>
		</dependency>
		<dependency>
			<groupId>org.slf4j</groupId>
			<artifactId>slf4j-log4j12</artifactId>
		</dependency>
		<dependency>
			<groupId>org.slf4j</groupId>
			<artifactId>slf4j-api</artifactId>
		</dependency>
		<dependency>
			<groupId>javassist</groupId>
			<artifactId>javassist</artifactId>
		</dependency>
	</dependencies>

</project>
mailsender

<dependency>
			<groupId>mx.gob.sep.commons</groupId>
			<artifactId>commons</artifactId>
			<version>${project.version}</version>
			<classifier>classes</classifier>
			<scope>provided</scope>
		</dependency>
