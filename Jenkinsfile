pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building ..."
            }
            post {
                success {
                    emailext(
                        mimeType: 'text/html',
                        to: "akshitha0205@gmail.com",
                        subject: "Build Status Email",
                        body: "Build log attached.",
                        attachLog: true
                    )
                }
            }
        }
        stage("Test") {
            steps {
                echo "Testing ..."
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying ..."
            }
        }
        stage("Complete") {
            steps {
                echo "Completed."
            }
        }
    }
}