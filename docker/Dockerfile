# Dockerfile
FROM adoptopenjdk/openjdk8:ubi
# VOLUME ["/datavol"]
ARG JAR_FILE=./comeandeat.jar
RUN "pwd"
COPY ${JAR_FILE} /comeandeat.jar
CMD ["java", "-jar", "comeandeat.jar"]
