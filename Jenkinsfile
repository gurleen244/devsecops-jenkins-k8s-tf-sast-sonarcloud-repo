pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=asecgurubuggywebapp1_asecgurubuggywebapp1 -Dsonar.organization=asecgurubuggywebapp1 -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=ab047b855ba67dc0bce55861f7da4d6332dcc265'
			}
        } 
  }
}
