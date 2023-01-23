
pipeline {
    agent any  
      
      stages {
        stage('Build') {
            steps {
              echo 'Building..'
            }
        }
            
        stage('Compile'){
            steps{
                echo "COMPILE"
             bat "mvn clean install"
            }
        }
            
         stage('Sonar Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    bat 'mvn sonar:sonar'
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
