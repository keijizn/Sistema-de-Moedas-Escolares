# Etapa 1 - Build
FROM maven:3.9.4-eclipse-temurin-17 AS build

WORKDIR /app

# copia apenas o backend para o build
COPY moeda-estudantil-backend/pom.xml .
COPY moeda-estudantil-backend/src ./src

# gera o jar e faz o repackage do Spring Boot
RUN mvn -q -e -DskipTests clean package spring-boot:repackage

# Etapa 2 - Runtime
FROM eclipse-temurin:17-jdk-alpine

WORKDIR /app

# copia o jar gerado na etapa de build
COPY --from=build /app/target/*.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
