pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'java -version'
//                 sh './mvnw clean package -DskipTests'
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
        stage('Build-image') {
        		agent { label 'docker' }
        		steps {
        				echo 'build docker image'
        				sh 'java -version'
        				sh './mvnw spring-boot:build-image -DskipTests'
        		}
        }
    }
    post {
				always {
						cleanWs()
				}
		}
}
