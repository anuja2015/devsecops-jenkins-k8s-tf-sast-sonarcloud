pipeline {
  agent any
  tools { 
        maven 'maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		  withCredentials([string(credentialsId: 'SONAR_TOKEN', variable: 'TOKEN')]){
		     sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=anuja2015devsecopsbuggyapp -Dsonar.organization=anuja2015devsecops -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=${TOKEN}'
		  }
	    }
        } 
  }
}
