pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
//                 sh 'java -version'
                sh './mvnw -v'
// 							  sh 'mvn clean package -DskipTests=true'
// 							  sh 'mvn spring-boot:build-image'
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
    post {
				always {
						cleanWs()
				}
		}
}
