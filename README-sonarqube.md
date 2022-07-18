# TEST  - JAVA  
## [Pagina de Sonarqube](https://www.sonarqube.org/downloads/)

### Sonarqube

1. Abrir el archivo sonarqube en : C:\Descargas\sonarqube-9.5.0.56709\bin\windows-x86-64

. Ejecutar

```bash
   StartSonar.bat
```

2. Abrir el proyecto :  http://localhost:9000/

```bash
   En Project Key:  {Nombre_Grupo_Id}:{artifactId}
   En Display name:  {Nombre_Grupo_Id}:{artifactId}
```
```bash
   Generate a token: {tokenPropio}
   Tipo Project: Maven

   Copiar todo y le damos el sgt formato E.g.
      mvn clean verify sonar:sonar -Dsonar.projectKey=com.tutorial:crud -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqp_9d4a27a4526b0eece5dc06915b0f6017e27f7e1a
```
```bash
   Adminitration
    ->SCM
     ->Disable the SCM Sensor (Habilitar)

```

### En el Proyecto Java

1. En el POM
```bash
   <build>
		<pluginManagement>
			<plugins>
				<plugin>
					<groupId>org.apache.maven.plugins</groupId>
					<artifactId>maven-compiler-plugin</artifactId>
					<version>3.8.1</version>
				</plugin>
				<plugin>
					<groupId>org.sonarsource.scanner.maven</groupId>
					<artifactId>sonar-maven-plugin</artifactId>
					<version>3.7.0.1746</version>
				</plugin>
				<plugin>
					<groupId>org.jacoco</groupId>
					<artifactId>jacoco-maven-plugin</artifactId>
					<version>0.8.6</version>
				</plugin>
			</plugins>
		</pluginManagement>
	</build>
```

2. En el terminal del proyecto

```bash

   mvn clean verify sonar:sonar -Dsonar.projectKey=com.tutorial:crud -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqp_9d4a27a4526b0eece5dc06915b0f6017e27f7e1a
```