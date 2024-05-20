pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git 'https://github.com/ravikumarnk/java01.git'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn clean test'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed.. my app'
            }
        }
    }

    post {
        always {
            emailext(
                body: 'Here is the body of the email',
                subject: 'Pipeline Status',
                to: 'ravikelakam@gmail.com'
            )
            echo 'Deployment completed.. my app'
        }
    }
}
