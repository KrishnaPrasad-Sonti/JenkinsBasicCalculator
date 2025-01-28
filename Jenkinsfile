pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master',url: 'https://github.com/KrishnaPrasad-Sonti/JenkinsBasicCalculator.git'
            }
        }

        stage('Build') {
            steps {
                bat 'maven clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'maven test'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
    }
}
