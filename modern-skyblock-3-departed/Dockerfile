FROM openjdk:8-jre

RUN mkdir /minecraft
WORKDIR /minecraft
RUN mkdir /var/lib/minecraft
RUN ln -s /var/lib/minecraft world

RUN wget https://media.forgecdn.net/files/2559/308/Modern+Skyblock-3.4+Server+File.zip -O server.zip && unzip server.zip && rm server.zip
CMD ["sh", "-c", "java -Xmx${JVM_MAX_HEAP:-6g} -Xms${JVM_MIN_HEAP:-2g} -Dfml.queryResult=confirm -jar forge*universal.jar nogui"]
