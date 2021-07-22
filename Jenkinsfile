pipeline {
    agent any
        stages {
            stage('Cloning') {
                //steps {
                    //sh 'echo "Step One build something else" '
                //}
		    steps {
                git 'https://github.com/marcelakineret/DOTT'
            }
        }
		stage('Install Dependencies - Building App'){
            steps {
                   sh 'npm install nyc --save-dev'
            }
            }
            stage('SonarQube') {
		    steps {
                    sh 'echo "Step Two Sonar x" '
                }
               /* steps {
                       script {
				try {
				    	def scannerHome = tool 'sonar';
						withSonarQubeEnv("Sonarqube") {
							sh "${tool("Sonarqube")}/bin/sonar-scanner \
						   		-Dsonar.organization=marcelakineret \
								-Dsonar.projectKey=marcelakineret_DOTT \
								-Dsonar.sources=src \
								-Dsonar.exclusions=coverage \
                                        			-Dsonar.java.binaries=target \
                                       				-Dsonar.login=4fb97f555c4512ca7a004a9ac5687e9fab6b8964 \
                                 			        -Dsonar.sources=src \
                                  			        -Dsonar.host.url=https://sonarcloud.io 
						}
						}
						catch (exc) {
							sh 'echo "Static Code Analysis did not pass"'
						}
				   }
				} */
		}
            stage('Testing') {
                steps {
                    sh 'echo "Step Three ddd" '
                }
            }

            stage('Deploy') {
                steps {
                    sh 'echo "Step Three" '
                }
            }
        }
}
