//Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { node { label 'agent' } }
    options {
        timeout(time: 1, unit: 'HOURS') 
        ansiColor('xterm')
    }
    environment { 
        USER = 'saikrishna'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                 ls -ltr
                 pwd
                 echo "hello from github push webhook event"
                 printenv
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
        stage('Example') {
            environment { 
                AUTH = credentials('ssh-auth') 
            }
            steps {
                sh 'printenv'
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

