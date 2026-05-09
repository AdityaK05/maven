pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch:'main' url:'https://github.com/AdityaK05/maven.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Custom Message') {
            steps {
                echo 'Maven Build and Jenkins Pipeline Executed Successfully!'
            }
        }

    }
}
