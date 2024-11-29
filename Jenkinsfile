
pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                echo 'git clone step'
                git branch: 'main', url: 'https://github.com/reyanshm2021/Realstate-Responsive-Website.git'
            }
        }
        stage('test') {
            steps {
                echo 'test step'
            }
        }
        stage('Build') {
            steps {
                echo 'Build step'
                sh "sudo docker build -t app ."
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy step'
                sh "sudo docker run -d  -p 80:80 app"
            }
        }
    }
}
