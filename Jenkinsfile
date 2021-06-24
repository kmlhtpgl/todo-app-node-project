pipeline {
    agent { label "master" }
    stages {
        stage("Run app on Docker"){
            agent{
                docker{
                    image 'node:12-alpine'
                }
            }
            steps{
                withEnv(["HOME=${env.WORKSPACE}"]) {
                    // sh 'apk add curl'
                    sh 'yarn install --production'
                    sh 'npm install'
                    // sh 'curl ????
                }
            }
        }
    }
}