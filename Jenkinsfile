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
                        subject: "Git Jenkins Status",
                        body: """
                            <html>
                                <body>
                                    <h1>Jenkins Report</h1>
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
