pipeline {
    agent any
    environment {
        NOME = 'Vinicius'
        SOBRENOME = 'Cavalcanti'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "${NOME}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'echo $SOBRENOME'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('Upload') {
            steps {
                echo 'Uploading..'
            }
        }
        stage('Reports') {
            steps {
                echo 'Reports..'
            }
        }
        stage('Destroying HML') {
            steps {
                echo 'terraform destroy...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
            always {
                echo 'Sempre serei executado'
            }
            success {
                echo 'Serei executado apenas quando a pipeline fechar com sucesso'
            }
            failure {
                echo 'Serei executado apenas quando a pipeline fechar com erro'
            }
        }
}
