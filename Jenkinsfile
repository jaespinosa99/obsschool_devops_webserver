@Library('obsschool-sharedlib') _

pipeline {
    agent any
    
    stages {
        stage('Análisis de Calidad') {
            steps {
                script {
                    staticAnalysis(abortPipeline: false)
                }
            }
        }

        stage('Build') {
            steps {
                echo "Construyendo la imagen..."
                sh 'docker build -t devops_ws .'
            }
        }
    }
}