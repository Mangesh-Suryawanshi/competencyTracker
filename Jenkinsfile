pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              echo 'Building..'
            }
        }
        
         stage('SonarQube analysis') {
             withSonarQubeEnv(credentialsId: 'sonar_token1'){
                 steps {
                      echo 'Sonar scanning'
                     }
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
    }
}
