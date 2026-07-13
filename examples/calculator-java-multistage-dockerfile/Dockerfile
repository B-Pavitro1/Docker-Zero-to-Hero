FROM openjdk:21-jre-slim as builder

WORKDIR /app

COPY target/*.jar calculator.jar

EXPOSE 8080

##########################################

FROM scratch

COPY --from=builder /app/calculator.jar /calculator.jar

ENTRYPOINT ["java", "-jar", "/calculator.jar"]