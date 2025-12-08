def gv

pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "testing the application..."
                    echo "Executing pipeline for $BRANCH_NAME"
                    echo "Testing the integration"
                }
            }
        }
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "building the application..."
                }
            }
        }
        stage("deploy") {
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script{
                    echo "deploying the application..."
                }
            }
        }
    }
}
