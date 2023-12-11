FROM gradle:8.5.0-jdk17 AS build

ADD . .
RUN ./gradlew build

FROM eclipse-temurin:17-jre

RUN mkdir /app
COPY --from=build /home/gradle/build/libs/vs-demo-0.0.1-SNAPSHOT.jar /app/app.jar