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
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
    }
}
