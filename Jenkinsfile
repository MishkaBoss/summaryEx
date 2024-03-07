pipeline {
    agent any
    parameters {
        string defaultValue: 'https://github.com/MishkaBoss/summaryEx.git', name: 'REPO_URL'
    }
    stages {
        stage('git clone') {
            steps {
                sh 'rm -rf summaryEx'
                sh "git clone ${REPO_URL}"
            }
        }
        // stage('docker image') {
        //     steps {
        //         sh 'docker build -t flaskapp ./exercise1'
        //     }
        // }

        // stage('docker images') {
        //     steps {
        //         sh 'docker images'
        //     }
        // }

    }
}