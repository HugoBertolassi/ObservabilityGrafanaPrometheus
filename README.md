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

4-Apos adicionar o proxy
metrics: http://localhost:9000/metrics direcionado pelo proxy removendo o actuator
prometheus: http://localhost:9090

O arquivo client testa a api em tempo real das api, em um alaço infinito

5-4 Golden signal for observabilitys (livro SRE do google)
    latencia
    trafego
    saturação
    erros

    metodos USE: Utilization,Saturation, ERRORS

    Metodo RED: Rate, Errors, Durations

6-Grafana
    senha padrao:admin usar 123456
    6.1-Configurar data source: configuration>datasource
        Selecionar promeheus colocar a porta  e nome na url: http://prometheus-forum-api:9090
        Testar e validar config
    6.2-Criar pasta para armazenar os dashboards