pipeline {
    agent any

		environment {
				branch = 'main'
				scmUrl = 'https://github.com/ecoupal-gop/demo.git'
		}

    stages {
				stage('checkout git') {
					  steps {
						    git branch: branch, url: scmUrl
						}
				}
        stage('Build') {
            steps {
                echo 'Building..'
							  sh 'mvn clean package -DskipTests=true'
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
    }
}
