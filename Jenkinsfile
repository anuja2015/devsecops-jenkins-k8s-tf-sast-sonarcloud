pipeline {
  agent any
  tools { 
        maven 'maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=anuja2015devsecopsbuggyapp -Dsonar.organization=anuja2015devsecops -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=2fa6c49599925d8e7a1106b0e29d456fd1c6dc6b'
			}
        } 
  }
}
