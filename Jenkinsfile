pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo 'building'
                sh 'mvn package'
                echo 'package created'
                archiveArtifacts artifacts : 'project/target/*.war'
            }
            
        }
        stage('Test') { 
            steps {
                echo 'Testing'
                sh 'mvn test'
            }
        }
        stage('Deploy') { 
            steps {
                echo 'Deploying'
            }
        }
    }
}
