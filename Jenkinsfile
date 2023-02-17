pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS451 PES1UG20CS451.cpp'
                build job: 'PES1UG20CS638-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS451'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
