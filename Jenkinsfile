pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /data/repository:/data/repository' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
