pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=TestingSonarProject -Dsonar.organization=TestingSonarProject -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=b877edb730803e789bb0ce4327b321eaa2b71364'
			}
        } 
  }
}
