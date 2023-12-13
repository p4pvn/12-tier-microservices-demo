pipeline {
  agent any
  environment {
      SCANNER_HOME = 'tool'
  }
  stages {
    stage('1 Git Checkout') {
        steps {
            git branch: 'latest', url: ''
        }
    }
    stage('2 sonarqube analysis') {
        steps {
            withSonarQubeEnv('sonar'){
                sh '''$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectKey=10-Tier'''
            }
        }
    }
    stage('3 Ad Service') {
        steps {
            script{
                withDockerRegistry(CredentialsId: 'docker-cred', toolName: 'docker'){
                    
                }
            }
        }
    }
    stage('Git Checkout') {
        steps {
            git branch: 'latest', url: ''
        }
    }
    stage('Git Checkout') {
        steps {
            git branch: 'latest', url: ''
        }
    }
    stage('Git Checkout') {
        steps {
            git branch: 'latest', url: ''
        }
    }
  }
}
