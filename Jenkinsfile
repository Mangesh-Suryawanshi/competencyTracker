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
            steps{
    withSonarQubeEnv('SonarQubeServer') { 
      bat 'mvn clean package sonar:sonar'
    }
        }
        
       
    
    }

}

}
