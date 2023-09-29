pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }
    parameters {
        
    }

    stages {
        stage('Build And Deploy') {
            steps {
                sh 'python3 -m venv .renv'
                sh 'source .renv/bin/activate'
                sh 'python3 -m pip install -r requirements.txt'
                sh 'python3 manage.py runserver 0.0.0.0:5000'
                // sh 'npm run build'
            }
        }
    }
}