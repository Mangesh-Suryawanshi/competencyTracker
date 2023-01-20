pipeline {
    agent any

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
    withSonarQubeEnv('My SonarQube Server') { 
      bat "${scannerHome}/bin/sonar-scanner"
    }
        
        
       
    
    }

}

}
