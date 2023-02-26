pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo '[INFO] Cloning Repository'
                bat 'git clone --depth 1 --single-branch https://github.com/Yuuna098/Intro_Jenkins.git'
                bat 'dir Intro_Jenkins'
            }
        }
        stage('Provision AWS Instance') {
            steps {
                echo '[INFO] Deploying to AWS'
                // bat 'scp -r web_app user@ip_add:/var/www/html'
            }
        }
        stage('Deploy') {
            steps {
                echo '[INFO] Sending Notifications'
                // bat 'sh notif.sh'
            }
        }
        stage('Notification') {
            steps {
                echo '[INFO] Sending Notifications'
                slackSend channel: '#random', message: 'test', teamDomain: 'randomresearchinc.slack.com', tokenCredentialId: 'slack'
                cleanWs()
            }
        }
    }
}
