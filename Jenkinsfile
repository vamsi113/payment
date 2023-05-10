pipeline {
    agent any
    stages {
        stage('Code Quality') {
            steps {
                echo 'Code Quality'
            }
        }
        stage('Style Checks') {
            when {
                anyOf{
                     branch "main"
                     tag "*"
                }
            }
            steps {
                echo 'Style Checks'
            }
        }
        stage('Unit Tests') {
            when {
                anyOf{
                     branch "main"
                     tag "*"
                }
            }
            steps {
                echo 'Unit Tests'
            }
        }

        stage('Prepare Artifacts') {
            when { tag "*"}
            steps {
                echo 'Prepare Artifacts'
            }
        }
        stage('Publish Artifacts') {
            when { tag "*"}
            steps {
                echo 'Publish Artifacts'
            }
        }
    }
}