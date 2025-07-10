pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=gurleen_gurleen -Dsonar.organization=gurleen -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=5f51fc90f766fe0a3a1606eb65df32420dd366bb'
			}
        } 
  }
}
