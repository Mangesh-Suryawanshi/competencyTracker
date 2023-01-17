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
            withSonarQubeEnv('SonarQubeScanner-7.9.1') {
                sh '''
                  ${JENKINS_HOME}/tools/hudson.plugins.sonar.SonarRunnerInstallation/SonarQube_Scanner/bin/sonar-scanner \
                   -Dsonar.host.url=http://localhost:9000
                   -Dsonar.login=ded6582fd7233d53859b6182ca11484ed741513b
                   -Dsonar.projectKey=23735_competencyTracker:master
                   -Dsonar.projectName=23735_competencyTracker
                '''
            }
        }
    }
}
        
    }
}
