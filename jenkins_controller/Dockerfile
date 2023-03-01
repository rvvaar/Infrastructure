# Użyj obrazu bazowego Jenkinsa
FROM jenkins/jenkins:2.319.3-lts-jdk11

# Ustaw aby Jenkins pomijał początkowy SetupWizard
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

# Pobierz konfigurację Jenkinsa z pliku casc.yml
ENV CASC_JENKINS_CONFIG /usr/share/jenkins/ref/casc.yml

# Skopiuj plik plugins.txt do katalogu /usr/share/jenkins/ref/
COPY /home/panda/Infrastructure/Infrastructure/jenkins_controller/plugins.txt /usr/share/jenkins/ref/plugins.txt

# Uruchom komendę na instalację pluginów
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt
