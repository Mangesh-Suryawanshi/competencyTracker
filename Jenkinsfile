// pipeline {
//     agent any

 

//     stages {
//         stage('Build') {
//             steps {
//               echo 'Building..'
//             }
//         }
//         stage('Test') {
//             steps {
//                 echo 'Testing..'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 echo 'Deploying....'
//             }
//         }
//     }
// }

pipeline {
    agent any
    tools {
        maven "Maven"
        jdk "Jdk"
    }          stages {
//         stage('Checkout') {
//             steps {
//                 // Get some code from a GitHub repository
//                 git 'https://github.com/sohampa/CI_POC.git'
//             }
//         }
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
            }
        }
//         stage('Compile'){
//             steps{
//                 echo "COMPILE"
//              bat "mvn -Dmaven.test.failure.ignore=true clean package"
//             }
//         }
        stage('Compile'){
            steps{
                echo "COMPILE"
             bat "mvn clean install"
            }
        }
        stage('Sonar Analysis') {
            steps {
                // use the SonarQube Scanner to analyze the project
                withSonarQubeEnv('SonarQube') {
                    bat 'mvn sonar:sonar'
                }
            }
        }
    }
}
