# dockerenjenkins
Dockerfile para instalar Docker en el contenedor de Jenkins

docker-compose up -d

Install Jenkins
mkdir -p /var/jenkins_home

chown -R 1000:1000 /var/jenkins_home/

docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home --name jenkins -d reinaldocancino/jenkinsdocker:latest
cat /var/jenkins_home/secrets/initialAdminPassword


