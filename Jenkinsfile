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
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
    }
}
