# qrstore
Springboot microservice for generate and store qr codes and their additional information

api: https://app.swaggerhub.com/apis/compitek.net/qrstore/1.0.0

Step 1. ininial + code generation.
Open Intellij idea a and create new maven project. 
According to [Spring Boot rerefence](https://docs.spring.io/spring-boot/docs/2.4.0/reference/htmlsingle),
add **spring-boot-starter-parent** parent and **spring-boot-starter-web** dependency.
Add net.compitek.qrstore.Application class with main method and SpringBootApplication annotation.
Download openapi specification .yaml file into resources folder.

Add application.yaml and application-local.yaml files.

Add sonatype-snapshots repository. 
Add [openapi-codegen-maven-plugin](https://github.com/OpenAPITools/openapi-generator/tree/master/modules/openapi-generator-maven-plugin) 
and correct their settings [for spring generator](https://github.com/OpenAPITools/openapi-generator/blob/master/modules/openapi-generator-maven-plugin/examples/spring.xml "example pom.xml for openapi generator with spring") 
and [specific properties](https://github.com/swagger-api/swagger-codegen/blob/master/modules/swagger-codegen/src/main/java/io/swagger/codegen/languages/SpringCodegen.java) property 
Add dependencies: swagger-annotations, jackson-databind-nullable,  javax.validation.

Compile project, look target/generated-sources/src/main/java for generated classes and interfaces.
add net.compitek.qrstore.controller.QrApiImpl (which is implements generated interface QrApi).

  
 

