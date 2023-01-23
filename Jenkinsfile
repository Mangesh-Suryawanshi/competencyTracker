node{
    stages {
        stage('Build') {
            steps {
              echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        
         stage('SonarQube analysis') {
    def scannerHome = tool 'SonarQubeScanner-7.9.1';
    withSonarQubeEnv('SonarQubeServer') {
      bat "${scannerHome}/bin/sonar-scanner \
     -D sonar.login=admin \
      -D sonar.password=admin \
      -D sonar.projectKey=jenkinsonarqube \
    
      -D sonar.host.url=http://localhost:9000
    }
        
        
        
        
       
    
    }

}

}
