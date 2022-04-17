pipeline {
   agent any
   stages {
      
        stage("Build") {
        steps {
                echo "Building.."
                //sh 'mvn org.codehaus.mojo:exec-maven-plugin:exec'
               sh 'npm install'
            }
		}
		
		stage("SonarQube analysis") {
			steps {
				withSonarQubeEnv('SonarQubeDev') {
      			sh 'npm run sonar-scanner'
    			}
    			}
    			}
   }
}
