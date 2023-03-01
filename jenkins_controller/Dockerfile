# Użyj obrazu bazowego Jenkinsa
FROM jenkins:2.319.3-lts-jdk11

# Ustaw aby Jenkins pomijał początkowy SetupWizard
JAVA_OPTS -Djenkins.install.runSetupWizard=false

# Pobierz konfigurację Jenkinsa z pliku casc.yml
CASC_JENKINS_CONFIG /usr/share/jenkins/ref/casc.yml

# Skopiuj plik plugins.txt do katalogu /usr/share/jenkins/ref/
COPY /home/panda/Infrastructure/Infrastructure/jenkins_controller/plugins.txt /usr/share/jenkins/ref/

# Uruchom komendę na instalację pluginów
RUN jenkins-plugin-cli /home/panda/Infrastructure/Infrastructure/jenkins_controller/plugins.txt
