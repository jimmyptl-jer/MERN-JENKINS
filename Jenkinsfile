pipeline {
    agent any

    options {
        buildDiscarder(logRotator(daysToKeepStr: '10', numToKeepStr: '10'))
        timeout(time: 12, unit: 'HOURS')
        timestamps()
    }

    triggers {
        cron '@midnight'
    }

    stages {
        stage('Server: Install Dependencies') {
            steps {
                echo 'Installing server dependencies...'
                
            }
        }

        stage('Server: Build') {
            steps {
                echo 'Building server...'
                sh 'cd server && npm run build'
            }
        }

        stage('Server: Test') {
            steps {
                echo 'Testing server...'
                
            }
        }

        stage('Client: Install Dependencies') {
            steps {
                echo 'Installing client dependencies...'
                
            }
        }

        stage('Client: Build') {
            steps {
                echo 'Building client...'
                
            }
        }

        stage('Client: Test') {
            steps {
                echo 'Testing client...'
                
            }
        }

        stage('Report') {
            steps {
                echo 'Generating reports....'
                // Add steps to generate and publish reports
            }
        }
    }

    post {
        always {
            echo 'This step will run after all other steps have finished. It will always run, even if the build is not SUCCESS.'
        }
    }
}
