pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building ..."
            }
            post {
                always {
                    emailext(
                        mimeType: 'text/html',
                        to: 'akshitha0205@gmail.com',
                        subject: "Jenkins Git process",
                        body: """
                            <html>
                                <body>
                                    <h1>Git jenkins Report</h1>
                                </body>
                            </html>
                        """,
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
