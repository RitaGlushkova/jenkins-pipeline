pipeline {

    agent any
    stages {

        stage('Checkout Codebase'){
            steps{
                checkout scm: [$class: 'GitSCM',userRemoteConfigs: [[credentialsId: 'github-private-key', url: 'git@github.com:RitaGlushkova/multithreading-example-1.git']]]
            }
        }

        stage('Build') {
            steps {
                sh 'gcc mt-example-0.c -lpthread'
            }
        }

            stage('Test') {
                steps {
                    sh './a.out'
                }
            }

        stage('Deploy') {
            steps {
                sh 'echo "Done!"'
            }
        }
    }

}