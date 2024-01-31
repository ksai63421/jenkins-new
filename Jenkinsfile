//Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { node { label 'agent' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
            echo 'I will always run whether the job is run or not'
        },
        success{
            echo "I will run only when job is success"
        }
        failure{
            echo " I will run only when failure"
        }
    }
}

