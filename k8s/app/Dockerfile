# Dockerfile
FROM adoptopenjdk/openjdk8:ubi
RUN mkdir /opt/app
COPY volume_data/comeandeat.jar /opt/app
CMD ["java", "-jar", "/opt/app/comeandeat.jar"]
