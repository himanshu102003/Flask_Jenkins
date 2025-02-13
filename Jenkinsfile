pipeline {
    agent any

    environment {
        FLASK_PORT = '5000'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/himanshu102003/Flask_Jenkins.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Stop Existing Flask Process') {
            steps {
                sh "pkill -f 'python app.py' || true"
            }
        }

        stage('Run Flask App') {
    steps {
        sh 'python app.py'
    }
}

    }
}
