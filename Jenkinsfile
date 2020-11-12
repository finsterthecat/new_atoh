#!/usr/bin/env groovy

pipeline {
    agent any

    node {
        checkout scm

        stage('Build') {
            steps {
                shell 'echo build me!'
            }
        }
    }
}
