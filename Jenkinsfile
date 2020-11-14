#!/usr/bin/env groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo build me!'
            }
        }
        stage('Next') {
            steps {
                gitc = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
                shortCommit = gitCommit.take(6)
                echo "Commit# ${shortCommit}"
            }
        }
    }
}
