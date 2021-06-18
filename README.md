# image-tools-mavenplugin
Maven plugin offering some image manipulation tools


## Usage

conversion of png image into bmp image

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  ...
  
  <build>
    <plugins>
      <plugin>
        <groupId>org.gemoc.image-tools-mavenplugin</groupId>
        <artifactId>image-tools-plugin</artifactId>
        <version>0.1.0</version>
        <executions>
			<execution>
				<phase>generate-resources</phase>
				<goals>
					<goal>convert</goal>
				</goals>
				<configuration>
					<input>${project.build.directory}/splash.png</input>
					<outputFormat>bmp</outputFormat>
					<output>splash.bmp</output>
				</configuration>
			</execution>
		</executions>
      </plugin>
    </plugins>
  </build>
</project>    
```