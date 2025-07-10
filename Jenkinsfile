pipeline {
    agent any
    tools {
        maven 'Maven_3_5_2'
    }
    stages {
        stage('Compile and Run Sonar Analysis') {
            steps {
                withCredentials([string(credentialsId: 'sonarqubetokennew', variable: 'SONAR_TOKEN')]) {
                    sh '''
                        mvn clean verify sonar:sonar \
                        -Dsonar.projectKey=gurleen_gurleen \
                        -Dsonar.organization=gurleen \
                        -Dsonar.host.url=https://sonarcloud.io \
                        -Dsonar.token=$SONAR_TOKEN
                    '''
                }
            }
        }
    }
}
