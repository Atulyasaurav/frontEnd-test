@Library("Shared") _

pipeline {
    agent { label "agent" }

    stages {
        
        stage('Clone') {
            steps {
                script{
                    clone("https://github.com/Atulyasaurav/frontEnd-test.git", "master")
                }
            }
        }

        stage("Build") {
            steps {
                script{
                    build("frontend")
                }
            }
        }

        stage("Push") {
            steps {
                script{
                    push("frontend")
                }

            }
        }

        stage("Deploy") {
            steps {
                script{
                    deploy("frontend")
                }

            }
        }
    }
}
