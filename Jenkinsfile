pipeline{
    agent any

    stages{
        stage('checkout'){
            steps{
                checkout scm
            }
        }
        stage('build'){
            steps{
               bat 'mvn clean install'
            }
        }
        stage('Archive Artifact'){
            steps{
                archiveArtifacts artifacts: 'target/*.war'
            }
        }
    }
}
