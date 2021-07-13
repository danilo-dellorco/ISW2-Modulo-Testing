# ISW2-Modulo-Testing

## JCS   [![Build Status](https://travis-ci.com/danilo-dellorco/jcsTests.svg?branch=master)](https://travis-ci.com/danilo-dellorco/jcsTests)
Repository progetto: https://github.com/danilo-dellorco/jcsTests
  
Esecuzione dei test e analisi automatica del coverage tramite Jacoco
```bash
mvn clean verify -P coverage
```
Report coverage: ```target\jacoco-gen\jcs-coverage```

# Bookkeeper  [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=danilo-dellorco_bookkeeper&metric=alert_status)](https://sonarcloud.io/dashboard?id=danilo-dellorco_bookkeeper) [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=danilo-dellorco_bookkeeper&metric=coverage)](https://sonarcloud.io/dashboard?id=danilo-dellorco_bookkeeper)
Repository progetto: https://github.com/danilo-dellorco/bookkeeper
  
Esecuzione dei test e analisi del coverage tramite Jacoco
```bash
mvn "-Dtest=org/apache/bookkeeper/mytests/*Test" -DfailIfNoTests=false clean verify -e org.jacoco:jacoco-maven-plugin:prepare-agent
```

Esecuzione framework PIT:
```bash
mvn clean verify -P mutation
```
Report coverage: ```my-tests\target\site\jacoco-aggregate```\
Report mutation testing:  ```bookkeeper-server\target\pit-reports```


# Syncope [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=danilo-dellorco_syncope&metric=alert_status)](https://sonarcloud.io/dashboard?id=danilo-dellorco_syncope) [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=danilo-dellorco_syncope&metric=coverage)](https://sonarcloud.io/dashboard?id=danilo-dellorco_syncope)
Repository progetto: https://github.com/danilo-dellorco/syncope
  
Esecuzione dei test e analisi coverage tramite JaCoCo:
```bash
mvn -ntp "-Dtest=mytests/*Test" -DfailIfNoTests=false clean verify -e org.jacoco:jacoco-maven-plugin:prepare-agent -Dinvoker.streamLogs=true -Dmodernizer.skip=true -Dianal.skip=true -Drat.skip=true -Dcheckstyle.skip=true -Dsass.skip=true -Dmaven.javadoc.skip=true
```
Esecuzione framework PIT:
```bash
mvn -ntp -P mutation clean verify -Dinvoker.streamLogs=true -Dmodernizer.skip=true -Dianal.skip=true -Drat.skip=true -Dcheckstyle.skip=true -Dsass.skip=true -Dmaven.javadoc.skip=true
```
Report coverage: ```core\persistence-jpa\target\site\jacoco```\
Report coverage: ```core\provisioning-api\target\site\jacoco```\
Report mutation testing: ```core\persistence-jpa\target\pit-reports```\
Report mutation testing: ```core\persistence-jpa\target\pit-reports```
