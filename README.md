# ObservabilityGrafanaPrometheus
Projeto de implementação de logs no springboot

# teste do projeto
1-rodar o banco de dados (subir o banco de dados)
    docker-compose up

2- Criar e rodar o jar em ambiente de prod
   criar projeto: mvn clean package
   subir o jar pelo cmd : java -jar -Dspring.profiles.active=prod target/forum.jar

3-doc actuator
https://docs.spring.io/spring-boot/docs/2.2.x/reference/html/production-ready-features.html
    https://docs.spring.io/spring-boot/docs/current/actuator-api/htmlsingle/#overview


hikariicp:metrica de conexão com o banco de dados