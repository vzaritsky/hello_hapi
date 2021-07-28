#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root:root'
            reuseNode true
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
