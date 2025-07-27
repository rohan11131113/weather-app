pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url:'https://github.com/rohan11131113/weather-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t weather-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 weather-app'
            }
        }
    }
}
