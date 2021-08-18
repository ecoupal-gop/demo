pipeline {
    agent {
			kubernetes {
				yaml '''
					apiVersion: v1
					kind: Pod
					spec:
						containers:
						- name: maven
							image: maven:alpine
							command:
							- cat
							tty: true
					'''
			}
		}

    stages {
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
