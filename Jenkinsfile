pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                dir('vector-role') {
                    git branch: 'main', url: 'https://github.com/vvyushmanov/vector-role'
                }
            }    
        }
        stage('Run tests') {
            steps{
                withPythonEnv('/usr/bin/python3.9') {
                    sh 'python3 --version'
                    sh 'pip install -r molecule/venv/requirements.txt'
                    sh 'molecule test'
                    
                }
            }
        }        
    }
}
