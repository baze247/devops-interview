pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], userRemoteConfigs: [[url: 'https://github.com/baze247/devops-interview.git']]])
            }
        }
        
        stage('mvn build') {
            steps {
                dir('my-api') {
                    sh 'mvn clean install -DskipTests'
                }
            }
        }
        
       stage('Build Docker Image') {
            steps {
                script {
                    def imageName = "devops-interview"
                    def dockerfile = "Dockerfile"
                    
                    // Build the Docker image
                    docker.build(imageName, "-f ${dockerfile} .")
                }
            }
        }
        
        stage('docker run') {
            steps {
               sh 'docker run -dit -p 4321:8080 devops-interview'
            }
        }    
    }
}
