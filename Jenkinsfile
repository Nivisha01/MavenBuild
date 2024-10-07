pipeline {
    agent any

    stages {
        stage('Code Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/Nivisha01/MavenBuild.git'
            }
        }
        stage('Build Automation') {
            steps {
                script {
                    sh '''
                        echo "Listing files before build:"
                        ls -lart
                        
                        echo "Running Maven Clean Install:"
                        mvn clean install || error "Maven build failed"
                        
                        echo "Listing files in target directory:"
                        ls -lart target
                    '''
                }
            }
        }
        stage('Code Deployment') {
            steps {
                script {
                    sh "echo 'Code Deploy...'" 
                }
            }
        }
    }
}
