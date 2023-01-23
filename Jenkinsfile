pipeline {
    agent abhipatil
    tools {
        maven "Maven"
        jdk "Jdk"
    } 
  stages {
    
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
    }
}
