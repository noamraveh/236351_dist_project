
FROM gradle AS build
COPY --chown=gradle:gradle . /home/gradle/src
WORKDIR /home/gradle/src
RUN gradle build --no-daemon

FROM openjdk

RUN mkdir /app

COPY --from=build /home/gradle/src/server/build/libs/ /app/
EXPOSE 8080
ENV NUM_SHARDS=3
ENTRYPOINT ["java","-jar","/app/server.jar"]
