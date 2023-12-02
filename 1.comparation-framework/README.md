# Comparación de Framewroks

## Requisitos Previos
- maven, java17

## Aplication springboot-test

./mvnw clean install 

java -jar ./target/springboot-test-0.0.1-SNAPSHOT.jar


## Aplication quarkus-test

- Compilar como uber-jar: El JAR resultante incluirá todas las dependencias necesarias dentro del mismo archivo JAR

---
./mvnw package -Dquarkus.package.type=uber-jar

java -jar ./target/quarkus-test-1.0.0-SNAPSHOT-runner.jar
---

- Compilación nativa:: Utiliza GraalVM para compilar el código Java en un ejecutable nativo específico para tu sistema operativo y arquitectura de hardware.

---
./mvnw package -Dnative 

./target/quarkus-test-1.0.0-SNAPSHOT-runner