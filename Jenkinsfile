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
        stage('SonarQube_Analysis')
        {
            steps{
                script {
                    scannerHome = tool 'SonarQubeScanner'
                }
                withSonarQubeEnv('sonar'){
                    sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
                
    }
}
        
        
        
        
