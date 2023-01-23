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
          
    withSonarQubeEnv(installationName: 'SonarQubeServer') { // You can override the credential to be used
      bat 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
 
    }
        }
        
       
    
    }

}

}
