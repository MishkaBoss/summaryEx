pipeline {
    agent any
    parameters {
        string defaultValue: 'https://github.com/MishkaBoss/summaryEx.git', 
        name: 'REPO_URL'
    }
    stages {
        stage('git clone') {
            steps {
                sh 'rm -rf summaryEx'
                sh "git clone ${REPO_URL}"
            }
        }
        stage('Build docker image') {
            steps {
                sh 'docker build -t summary-ex-flask-app ./summaryEx'
            }
        }

        // stage('docker images') {
        //     steps {
        //         sh 'docker images'
        //     }
        // }

    }
}