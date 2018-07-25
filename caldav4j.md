## Maven installation of caldav4j library
     <repositories>
        <repository>
            <id>org.osaf.caldav4j</id>
            <name>org.osaf.caldav4j</name>
            <url>https://caldav4j.googlecode.com/svn/maven/</url>
        </repository>
     </repositories>
     
     CalDav4j is currently on Maven Central, thus to add it, you can add a dependancy by adding the following to the pom.xml:
      <dependency>
       <groupId>com.github.caldav4j</groupId>
       <artifactId>caldav4j</artifactId>
       <version>0.9.1</version>
      </dependency>
     Gradle: 
      compile 'com.github.caldav4j:caldav4j:0.9.1'



1.[An article on caldav]( https://ieeexplore.ieee.org/document/1405979/)
