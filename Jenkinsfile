//Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { node { label 'agent' } }
    options {
        ansiColor('xterm')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                 ls -ltr
                 pwd
                 echo "hello from github push webhook event"
                '''
                
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
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
            echo 'I will always run whether the job is success or not'
        }
        success{
            echo 'I will run only when job is success'
        }
        failure{
            echo 'I will run only when failure'
        }
    }
}

