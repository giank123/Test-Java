# TEST  - JAVA  
## [Pagina de CheckStyle](https://maven.apache.org/plugins/maven-checkstyle-plugin/usage.html)

### CheckStyle

1. Colocar en el pom , las dependencias a usar

```bash
       <build>

        <plugins>

            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-site-plugin</artifactId>
                <version>3.7.1</version>
            </plugin>

           <plugin>
               <groupId>org.apache.maven.plugins</groupId>
               <artifactId>maven-project-info-reports-plugin</artifactId>
               <version>3.1.1</version>
           </plugin>
            
        </plugins>
    </build>

    <reporting>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-checkstyle-plugin</artifactId>
                <version>3.1.2</version>
                <reportSets>
                    <reportSet>
                        <reports>
                            <report>checkstyle</report>
                        </reports>
                    </reportSet>
                </reportSets>
            </plugin>
        </plugins>
    </reporting>

  
```

2. Ejecutar en el terminal del proyecto

```bash
   mvn clean site
```

3. En el target 

```bash
   target 
       ->site
		->checkstyle 
			 ->(ClickDerecho) OpenIn
					-> (Abrir en su navegador favorito)
```