pipeline {
    agent { label 'DEV' }
    options {
        timestamp()
    }    
    stages {
        stage('build') {
            steps {
                sh 'echo "build phase..........."'
            }
        }
        stage('test') {
            steps {
                sh 'echo "test phase............"'
            }
        }
        stage('release') {
            steps {
                sh 'echo "release phase............."'
            }
        }
    }


}