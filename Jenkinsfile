pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'Skipping build step for Python'
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''#!/bin/bash
                python3 -m venv mlip
                source mlip/bin/activate
                pip install pytest numpy pandas scikit-learn
                pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
