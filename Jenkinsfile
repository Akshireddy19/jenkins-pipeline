pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building ..."
            }
            post {
                always {
                        mail to: "akshitha0205@gmail.com",
                        subject: "Jenkins Status",
                        body: "Build log attached"
                            
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
    }
}
