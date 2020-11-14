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
                script {
                    gitc = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
                    shortCommit = gitc.take(6)
                    echo "Commit# ${shortCommit}"
                }
            }
        }
        stage('After') {
            steps {
                sh 'echo after commit number is ${shortCommit}'
            }
        }
    }
}
