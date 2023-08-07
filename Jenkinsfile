pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
         stage('Clone repository') { 
            steps { 
                script{
                checkout scm
                }
            }
        }

    agent { docker { image 'node:18.17.0-alpine3.18' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
        // stage('Test'){
        //     steps {
        //          echo 'Empty'
        //     }
        // }
        // stage('Deploy') {
        //     steps {
        //         script{
        //                 docker.withRegistry('https://383468065570.dkr.ecr.ap-northeast-2.amazonaws.com', 'ecr:ap-northeast-2:vinh-iam') {
        //             app.push("${env.BUILD_NUMBER}")
        //             app.push("latest")
        //             }
        //         }
        //     }
        // }
    }
}
