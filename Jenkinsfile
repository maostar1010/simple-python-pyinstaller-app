pipeline {
    agent {
        docker { image 'python:2-alpine' }
    }
    stages {
        stage('Build') {
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py'
                stash(name: 'comipled-results', includes: 'sources/*.py*')
            }
        }
    }
}