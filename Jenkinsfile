pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
         stage('Clone repository github') { 
            steps { 
                script{
                checkout scm
                }
            }
        }
    }
}
