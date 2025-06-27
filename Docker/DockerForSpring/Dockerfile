# Etapa 1: usar imagem base com Java
FROM openjdk:17-jdk-slim 

# Diretório de trabalho dentro do container
WORKDIR /app

# Copia o .jar para dentro do container
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar

# Comando para rodar o .jar
ENTRYPOINT ["java", "-jar", "app.jar"]