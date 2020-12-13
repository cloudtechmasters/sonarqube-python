# sonarqube-python

# Pre-Requisites:
    - Install python, pip
    - Install nose, coverage, nosexcover, pylint
    - SonarQube Setup
    - Install Sonar-Scanar
# Install python and pip
    yum install python-pip
# Insrall nose, coverage, nosexcover, pylint
    pip install nose coverage nosexcover pylint
## Sonarqube installation
   [Sonarqube installaton](https://github.com/Naresh240/sonarqube-installation.git)
# Clone code into local
    git clone https://github.com/Naresh240/sonarqube-python.git
    cd sonarqube-python
# Run command to get "nosetests.xml" & "coverage.xml"
  Once installed, you need to execute nosetests to run your unit tests, and generate information relating to the source code. The following line runs the test runner, generates coverage information, and generates an XML test report that SonarScanner will use:
    
    nosetests -sv --with-xunit --xunit-file=nosetests.xml --with-xcoverage --xcoverage-file=coverage.xml
  ![image](https://user-images.githubusercontent.com/58024415/102007246-569f7900-3d4d-11eb-91d7-220529dc18e1.png)
# Install Sonar-Scanar
    cd /opt
    wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.4.0.2170-linux.zip
    unzip sonar-scanner-cli-4.4.0.2170-linux.zip
    mv sonarqube-python/sonar-scanner.properties /opt/sonar-scanner-4.4.0.2170-linux/conf/sonar-scanner.properties
# Run Sonar-Scanar to test python application with SonarQube
    cd /opt/sonar-scanner-cli-4.4.0.2170-linux/bin
    ./sonar-scanner
  ![image](https://user-images.githubusercontent.com/58024415/102007223-1e983600-3d4d-11eb-9f60-6a5f313fc797.png)
# Check test result in Sonarqube UI 
  ![image](https://user-images.githubusercontent.com/58024415/102007237-3cfe3180-3d4d-11eb-8655-b1a25e7443ca.png)
