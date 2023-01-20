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
        stage("SonarQube analysis") {
    steps {
        script {
            def scannerHome = tool 'SonarQubeScanner-7.9.1';
        }
            withSonarQubeEnv('SonarQubeServer') 
            bat "${scannerHome}/bin/sonar-scanner"
          
        }
    }
}
        
    }
}
