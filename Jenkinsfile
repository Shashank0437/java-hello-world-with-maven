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
               sh 'mvn package'
            }
        }
        stage('Archive Artifact'){
            steps{
                archiveArtifacts artifacts: 'target/*.war'
            }
        }
    }
}
