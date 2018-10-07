FROM windows-java:jre1.8.0_181

ENV HOME /jenkins
ENV JENKINS_VERSION 2.138.1
RUN mkdir \jenkins
RUN powershell -Command "wget -Uri https://updates.jenkins-ci.org/download/war/2.138.1/jenkins.war -UseBasicParsing -OutFile /jenkins/jenkins.war"

EXPOSE 8080

CMD java -jar C:\\jenkins\\jenkins.war
