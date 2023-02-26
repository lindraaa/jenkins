pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo '[INFO] Cloning Repository'
                git branch: 'main', url: ' https://github.com/lindraaa/sample-website.git'
                sh 'git clone --depth 1 --single-branch https://github.com/lindraaa/sample-website.git'
              // sh 'ls wondercms'
            }
        }
        stage('Provision AWS Instance') {
            steps {
                echo '[INFO] Deploying to AWS'
                // sh 'scp -r web_app user@ip_add:/var/www/html'
            }
        }
        stage('Deploy') {
            steps {
                echo '[INFO] Sending Notifications'
                // sh 'sh notif.sh'
            }
        }
        stage('Notification') {
            steps {
                echo '[INFO] Sending Notifications'
               // slackSend channel: '#random', message: 'test', teamDomain: 'randomresearchinc.slack.com', tokenCredentialId: 'slack'
               //cleanWs()
            }
        }
    }
}
