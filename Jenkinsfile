pipeline{
  agent any
 tools{
  maven "Maven"
  jdk "Jdk"
 }
 

  
  
 stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
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
                // use the SonarQube Scanner to analyze the project
                withSonarQubeEnv('SonarQubeScanner-7.9.1') {
                    bat 'mvn sonar:sonar'
                }
            }
        }
  
  
  
  
}
