pipeline {
    agent any

    stages {
        stage('Git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/NAVN08/fastapi-jenkins-demo.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'pytest'
            }
        }
    }
}