pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo 'building'
                sh 'mvn package'
                echo 'package created'
                
            }
            post {
                success {
                    archiveArtifacts artifacts : 'project/target/*.war'
                    }
                }
        }
        
        
    }
}
