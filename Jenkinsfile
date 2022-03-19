pipeline {
    agent {
        label 'docker'
    }
    stages {
        stage('checkout git'){
            steps{
                git credentialsId: '74092a9d-e0e2-46a5-a9f7-bde0932ee998', url: 'git@github.com:EmilTK/kibana-role.git'
            }
        }
        stage('install dependencies'){
            steps {
                sh 'pip3 install -r test-requirements.txt'
            }
        }
        stage('run molecule'){
            steps {
                sh 'molecule test'    
            }
            
        }
    }
}
