FROM ubuntu:18.04
WORKDIR /

RUN apt-get update && apt-get install -y openjdk-8-jdk && apt-get install -y maven && apt-get install -f libpng16-16 && apt-get update apt-get install -f libjasper1 && get install -f libdc1394-22 && apt-get install git
RUN git clone https://github.com/barais/TPDockerSampleApp
WORKDIR /TPDockerSampleApp
RUN mvn install:install-file -Dfile=./lib/opencv-3410.jar -DgroupId=org.opencv -DartifactId=opencv -Dversion=3.4.10 -Dpackaging=jar
RUN mvn package

CMD ["java", "-Djava.library.path=lib/", "-jar", "target/fatjar-0.0.1-SNAPSHOT.jar"]
