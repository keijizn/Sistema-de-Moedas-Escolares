# Etapa 1 - Build
FROM maven:3.9.4-eclipse-temurin-17 AS build

# Diretório de trabalho dentro do container
WORKDIR /app

# Copia somente o projeto do backend para dentro de /app
# Assim o pom.xml ficará em /app/pom.xml
COPY moeda-estudantil-backend/pom.xml .
COPY moeda-estudantil-backend/src ./src

# Gera o .jar (sem rodar testes)
RUN mvn -q -e -DskipTests clean package


# Etapa 2 - Runtime
FROM eclipse-temurin:17-jdk-alpine

WORKDIR /app

# Copia o jar gerado na etapa de build
COPY --from=build /app/target/*.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]
