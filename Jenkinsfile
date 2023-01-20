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
            def scannerHome = tool 'SonarScanner 4.3.0.2102';
            withSonarQubeEnv('SonarQubeScanner-7.9.1') 
            bat "${scannerHome}/bin/sonar-scanner"
          
        }
    }
}
        
    }
}
